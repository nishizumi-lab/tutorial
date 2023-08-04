# 【Flutter入門】AndroidアプリをGoogle Playで公開する方法

## Google Playデベロッパーアカウントの作成(初回のみ)

AndroidアプリをGoogle Playで公開するには、Google Playデベロッパーアカウントの作成が必要です。
Google Playデベロッパーアカウント登録には25＄必要になります。

- Googleアカウントにログインします。
（Googleアカウントがない場合は事前に作成）

- Google Play デベロッパーコンソールのページ[https://play.google.com/apps/publish/signup/](https://play.google.com/apps/publish/signup/)を開きます。

- 「Google Play デベロッパー販売/配布契約書に同意し、自分のアカウント登録を関連付けることを希望します。」にチェックをいれます。

- 「支払いに進む」を選択します。

- お支払情報を入力していきます。（カード番号など）「支払う」ボタンを押します。


- 「デベロッパー名」「メールアドレス」「電話番号」を入力して「登録を終了」ボタンをクリックします。

※電話番号は次のように入力します。

自宅・・・03-1234-5678 → +81-3-1234-5678

携帯・・・090-1234-5678　→ +81-90-1234-5678

- これで登録完了となります。

## Google Playで公開する手順

- keystoreファイル（署名するときの設定ファイル）を作成し、「android\app\key.jks」に配置します。

```
keytool -genkey -v -keystore key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
```

- android/keystore.properties を新規作成し、以下のように中身を記述します。

```
storePassword=ストアのパスワード
keyPassword=キーのパスワード
keyAlias=エイリアス名
storeFile=keystoreファイルのパス
```

- android/app/build.gradle を以下のように編集します。

```
def localProperties = new Properties()
def localPropertiesFile = rootProject.file('local.properties')
if (localPropertiesFile.exists()) {
    localPropertiesFile.withReader('UTF-8') { reader ->
        localProperties.load(reader)
    }
}

def flutterRoot = localProperties.getProperty('flutter.sdk')
if (flutterRoot == null) {
    throw new GradleException("Flutter SDK not found. Define location with flutter.sdk in the local.properties file.")
}

def flutterVersionCode = localProperties.getProperty('flutter.versionCode')
if (flutterVersionCode == null) {
    flutterVersionCode = '1'
}

def flutterVersionName = localProperties.getProperty('flutter.versionName')
if (flutterVersionName == null) {
    flutterVersionName = '1.0'
}

apply plugin: 'com.android.application'
apply plugin: 'kotlin-android'
apply from: "$flutterRoot/packages/flutter_tools/gradle/flutter.gradle"

// 追加①
def keystorePropertiesFile = rootProject.file("keystore.properties")

android {
    compileSdkVersion 30

    sourceSets {
        main.java.srcDirs += 'src/main/kotlin'
    }

    defaultConfig {
        // TODO: Specify your own unique Application ID (https://developer.android.com/studio/build/application-id.html).
        applicationId "jp.co.orust.kinkyu"
        minSdkVersion 16
        targetSdkVersion 30
        versionCode flutterVersionCode.toInteger()
        versionName flutterVersionName
        multiDexEnabled true // 追加②
    }

    // ここから追加③
    signingConfigs {
        release {
            if (keystorePropertiesFile.exists()) {
                def keystoreProperties = new Properties()
                keystoreProperties.load(new FileInputStream(keystorePropertiesFile))
                keyAlias keystoreProperties['keyAlias']
                keyPassword keystoreProperties['keyPassword']
                storeFile file(keystoreProperties['storeFile'])
                storePassword keystoreProperties['storePassword']
            }
        }
    }
    // ここまで追加③
    buildTypes {
        release {
            signingConfig signingConfigs.release // 変更①
        }
    }
}

flutter {
    source '../..'
}

dependencies {
    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
}
```

パラメータ|説明
--|--
password|keystoreファイル作成時に設定したパスワード
alias-name|エイリアス名
key.js|作成したkeystoreファイルのパス

- AndroidManifest.xmlにもApp Bundle のパッケージ名(xxx.yyy.zzzなど)を挿入します。

■android\app\src\main\AndroidManifest.xml
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="xxx.yyy.zzz">


- 以下のコマンドをAndroid Studioのターミナルで実行すると、「build\app\outputs\apk\release\app-release.apk 」にapkファイルが作成されます。

```
flutter build apk --release
```

- アプリの更新をするときは、アプリのバージョン番号とバージョンコードの値も上げてやる必要があります。変更は、pubspec.yamlで行います。

```
name: アプリ名
description: A new Flutter application.
publish_to: 'none' # Remove this line if you wish to publish to pub.dev
version: バージョン番号+バージョンコード
```

## Android App BundleでGoogle Playに公開

Android App Bundleとは、ユーザー毎に最適なapkを作成（ビルド）し配信する仕組みです。
Android App Bundle の形式のファイルの拡張子は .aabで、32bit、64bitのAPKなどがすべて入っており、Google Playはそこから必要なリソースを取り出してapkをユーザーに再構築して配信します。
そのため、ユーザー側には必要なリソースだけが含まれるapkがインストールされるので、アプリサイズの削減につながる利点があります。
ただし、 Android App Bundle を利用するためにはGoogle Play側でapkの再構築と署名を行うため、 Google Play App Signing を使う必要があります。

https://algorithm.joho.info/flutter/google-play-app-signing/

- Flutterでは、バージョン1.7からAndroid App Bundleに対応しています。

```
flutter build appbundle --release
```

## APKファイルのアップロード

- Google Play デベロッパーコンソールにログインします。

- 「Google Playにアプリを追加」　ボタンをクリックします。

- 「言語」「タイトル」を入力して「作成」ボタンをクリックします。

-  「タイトル」「簡単な説明」「詳細な説明」 「画像および動画（スクショ）」「高解像度アイコン」「宣伝用画像」「アプリのタイプ」「カテゴリ」「コンテンツレーティング」「ウェブサイト」「メール」「プライバシー ポリシー」を入力します。

- 左メニューから「APK」を選択します。

- 「製品版に最初のAPKをアップロード」ボタンをクリックしてAPKファイルを選択し、アップロードします。

※「ベータ版」「アルファ版」でアップロードすると公開範囲を制限できます

※エラーが出た場合の対処法については下記事にまとめています。

- アップロードが終わった後、いよいよ公開していきます。左メニューから「価格と販売/配布地域」を選択します。

- 「アプリの価格の設定」で「有料」か「無料」を選択します。

※「有料」が選択できない場合は「今すぐ販売アカウントをセットアップする」をクリックして販売アカウントを登録します

- 「CREATE A NEW MERCHANT ACCOUNT」のみが表示される場合、「配布する地域」などのチェックをしてから「今すぐ販売アカウントをセットアップする」を再度クリックします。

- 必要事項を入力します。

- 「同意」にチェックをいれます。

- 「登録を完了する」ボタンをクリックします。

- 「配布する地域」などをチェックをします。

- 「保存」ボタンをクリックします。

- 左メニューの「APK」「ストアの掲載情報」「価格と販売/配布地域」のチェックマークがすべて緑色になります。

- 画面右上の「公開の準備完了」をクリックします。

- 「このアプリを公開する」を選択します。

- アプリが公開されます。

## Google Playで非公開・削除

Google Playに投稿したアプリを非公開（削除）する手順は次のとおりです。

-  [Google Play Console]にログインし、非公開・削除したいアプリのトップページを開きます。

- 左側メニューから[ストアでの表示]→[価格と販売 / 配布地域]を選択します。

- アプリの公開状況を[非公開]に変更します。

- ページをスクロールし「確認」ボタンを押します。

- [アップデートを送信]ボタンを押します。

-  アプリのステータスが[公開停止中]になれば成功です。

