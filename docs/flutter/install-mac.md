# 【Flutter】M1・M2 Macにインストールする方法


## Flutterのインストール手順

-  「Android Studio + Android SDK + Build-Tools」をインストールしていない場合、インストールします。方法は以下ページで紹介しています。

[【M1・M2 Mac】Android Studioのインストール方法]()

- 「Xcode」をインストールしていない場合、インストールします。方法は以下ページで紹介しています。

[【M1・M2 Mac】Xcodeのインストール方法]()

- Android Studioを起動し、「Configure」→「Plugins」を開きます

- 2つのプラグイン「Flutter」「Dart」をインストールします。

- Android Studioを再起動し、「Flutterプロジェクト」を作成します。

- 公式HP([https://flutter.io/]（https://flutter.io/）)の[Get started]をクリックし、Flutter SDKをダウンロードします。ダウンロードしたファイルを解凍して任意のディレクトリに置きます。

- ターミナルを開いてFlutterのパスを設定します。

【bashの場合】

```
echo 'export PATH="$PATH:[flutterディレクトリを配置している絶対パス]/flutter/bin"' >> ~/.bash_profile
source ~/.bash_profile
```

【zshの場合】

```
echo 'export PATH="$PATH:[flutterディレクトリを配置している絶対パス]/flutter/bin"' >> ~/.zshrc
source ~/.zshrc
```

【.zshrcの例】

```
export PATH=$PATH:/Users/libs/flutter/bin
```


- コマンドプロンプトで以下のコマンドを実行し、ヘルプが表示されたらパス設定は成功です。

```
$ flutter
```

- Flutterで環境構築が正常にできたか確認するために「flutter doctor」を実行したとき、以下のようにAndroid toolchainのライセンス承諾ができていないと出ることがあります。

```
$ flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, 1.25.0-8.2.pre, on macOS 11.1 20C69 darwin-arm,
    locale ja-JP)
[!] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
    ! Some Android licenses not accepted.  To resolve this, run: flutter doctor
      --android-licenses
[✓] Xcode - develop for iOS and macOS (Xcode 12.3)
[✓] Android Studio (version 4.1)
[✓] VS Code (version 1.52.1)
[✓] Connected device (1 available)

! Doctor found issues in 1 category.
```

- 以下のコマンドを実行し、「y」を押して同意していくと問題が解決します。

```
$ flutter doctor --android-licenses
```

- もし以下のようなエラーが出た場合、「Android Studio configure」 > 「SDK Manager」 > 「SDK Tools」を開きます。

- 「Android SDK Command-line Tools(latest)」にチェックを入れます。

- 「Hide Obsolete Packages」のチェックを外します。

- 「Android SDK Tools(Obsolete)」をクリックして「OK」ボタンを押して「flutter doctor --android-licenses」を実行しなおします。


```
$ flutter doctor --android-licenses
Exception in thread "main" java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema
    at com.android.repository.api.SchemaModule$SchemaModuleVersion.(SchemaModule.java:156)
    at com.android.repository.api.SchemaModule.(SchemaModule.java:75)
    at com.android.sdklib.repository.AndroidSdkHandler.(AndroidSdkHandler.java:81)
    at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:73)
    at com.android.sdklib.tool.sdkmanager.SdkManagerCli.main(SdkManagerCli.java:48)
Caused by: java.lang.ClassNotFoundException: javax.xml.bind.annotation.XmlSchema
    at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:581)
    at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:178)
    at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:522)
    ... 5 more
```

```
$ flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel beta, 1.25.0-8.2.pre, on macOS 11.1 20C69 darwin-arm,
    locale ja-JP)
[✓] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
[✓] Xcode - develop for iOS and macOS (Xcode 12.3)
[✓] Android Studio (version 4.1)
[✓] VS Code (version 1.52.1)
[✓] Connected device (1 available)

• No issues found!
```

- Android StudioのFlutterプロジェクト作成画面で「Flutter SDK Path」に「flutterディレクトリを配置している絶対パス/flutter/bin」を指定してやります。

## 関連ページ

[【Flutter入門】iOS、Android、Windowsアプリを効率よくまとめて開発](./index.md)
