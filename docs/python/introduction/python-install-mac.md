# 【M1・M2 Mac】Pythonをインストールして使う方法

## 【方法1】標準搭載されているPythonを使う(初級者向け)

Mac OSでは、デフォルトでPythonがインストールされています。
Pythonにはバージョン2とバージョン3の2種類があります。
注意点として、最新版のMac OS(Ventura)では、バージョン2とバージョン3の2種類があります。
余程のことがない限り、バージョン3を使うのをおすすめします。

【バージョン3のPythonを実行する方法】

- 適当なテキストエディタで、以下の内容を記述したPythonファイル(test.py)を作成します。


```
print("hello world")
```

- ターミナルを開き、以下のコマンドを実行します。

```
$ python3 [Pythonファイルのパス]/test.py
```

- 補足
    - 例えばダウンロードフォルダにtest.pyを保存した場合は「$ python3 /Users/ユーザー名/Downloads/test.py」となります。
    - パスを入力するのがめんどくさい場合は、pythonファイルをターミナルにドラッグ＆ドロップするとパスが自動的に表示されます。
    - バージョン2のPythonで実行したい場合、「$ python [Pythonファイルのパス]/test.py」で実行します。

- 「hello world」と表示されたら成功です。Pythonを実行できたことになります。なお、標準でインストールされているPythonのバージョンは「python --version」で確認できます。

```
$ python3 --version

python 3.9.5
```

## 【方法2】Google Colaboratoryを使う(初級者〜上級者向け)

Google Colaboratoryという、クラウドサービスを使えば、インストール作業の必要もなく、WebブラウザだけでPythonを実行できます。インストール作業に不安のある初級者から、GPUが搭載されていないモバイルPCで本格的な機械学習をしたい中上級者にもおすすめです。詳細は以下ページで紹介しています。

- [【Google Colaboratory】WebブラウザでPythonを使う方法](./colaboratory.md)


## 【方法3】最新版のPythonをインストールして使う(中級者向け)

Python.org（公式）より、最新版のPython3をインストールする方法は以下のとおりです。

- 公式ページ[https://www.python.org/downloads/](https://www.python.org/downloads/)を開き、最新バージョンの[Download]をクリックしてdmgファイルをダウンロードします。

- ダウンロードしたdmgファイルを実行し、Pythonをインストールします。


## 【方法4】Homebrewを使用したPythonのインストール方法(上級者向け)

MacにはデフォルトでPython環境がインストールされています。
しかし、システムの安全性や利便性等を考えると「homebrew」「pyenv」「virtualenv」を用いた仮想環境上でPython3をインストールして利用するのがおすすめです。
プログラミングに慣れている人は、パッケージ管理システム(Homebrew)を使用し、複数のバージョンのPythonをインストールして管理しています。

以下のような導入手順となります。

- App Store[https://apps.apple.com/jp/app/xcode/id497799835](https://apps.apple.com/jp/app/xcode/id497799835)からXcodeをインストールします。

- ターミナルを起動し、以下のコマンドでXCodeのCommand Line Toolsをインストールします。

```
$ xcode-select --install
```

- 「公式サイト」に掲載されているインストール用のコマンドをコピーし、ターミナルで実行します。

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- 「Installation successful!」と表示されたら成功です。ターミナルで以下のコマンドを実行すれば、正常にHomebrewをインストールできたか確認できます。

```
$ brew doctor
```

- pyenvは、Pythonのバージョンを切り替えるためのツールです。以下のコマンドでpyenvをインストールします。

```
export PYENV_ROOT=/usr/local/var/pyenv
if which pyenv > /dev/null; then eval "$(pyenv init -)"; fi
```

```
$ brew install pyenv
```

