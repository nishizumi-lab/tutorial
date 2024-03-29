# 【Python】Windowsへ簡単にインストールする方法を紹介

## 各種インストール方法の比較

WindowsにPythonの開発環境を構築する方法は以下のとおりいくつかあります。

- 公式インストーラ(定番)
    - 普通のソフトと同じように、公式HPから実行ファイルをダウンロードしてインストールする方法です。
- Google Colaboratory
    - Google Colaboratoryという、クラウドサービスを使えば、インストール作業の必要もなく、WebブラウザだけでPythonを実行できます。インストール作業に不安のある初級者から、GPUが搭載されていないモバイルPCで本格的な機械学習をしたい中上級者にもおすすめです。
- Pythonパッケージ
    - Python単体だけでなく、定番の外部モジュールを一緒にインストールしてくれる便利なパッケージです。「WinPython」や「Anaconda(Miniconda)」など、Pythonパッケージには様々な種類があるため、ある程度利用目的が決まっていて、Pythonパッケージ特有のトラブルにも対処できるプログラミング中級者〜上級者向きです。
- WSL(Windows Subsystem for Linux)
    - Windowsに標準搭載されているLinux仮想環境であるWSLにPythonをインストールして使う方法です。Pythonの外部モジュールの中には、Linux上でしか動作しないものもあり、そういったものを使う場合に利用したりします。仮想環境上で実行するため、各種設定やトラブルに対処できるプログラミング中級者〜上級者向きです。
- Docker
    - コンテナ型の仮想環境Docker上でPython環境を構築する方法です。プログラミング上級者向きです。

## 【方法1】公式インストーラーでインストール

- 公式インストーラーでインストールする方法は以下ページで解説しています。

- ある程度、Pythonに使い慣れてきたら、VSCode(Visual Studio Code)でコードを書いて実行するのがおすすめです。VScodeには、Pythonの開発を快適に行える様々な拡張機能があり、効率よく中～大規模なPythonプログラムを構築できます。導入方法は以下ページで解説しています。

- [【Windows11】標準インストーラでPythonをインストールする方法](./python-standard-install-windows.md)

## 【方法2】Google Colaboratoryを使う

Google Colaboratoryという、クラウドサービスを使えば、インストール作業の必要もなく、WebブラウザだけでPythonを実行できます。インストール作業に不安のある初級者から、GPUが搭載されていないモバイルPCで本格的な機械学習をしたい中上級者にもおすすめです。詳細は以下ページで紹介しています。

- [【Google Colaboratory】WebブラウザでPythonを使う方法](./colaboratory.md)

## 【方法3】Pythonパッケージでインストール

- プログラミング中級者以上の方で、「**Pythonで機械学習やデータ分析をしてみよう、でも1からPythonを入れたり外部モジュールをインストールするのは面倒だな**」という方は、「WinPython」「Miniconda」「Anaconda」といったPythonパッケージで環境構築するのがおすすめ。
- 
（Anacondaは高機能だが独自機能の要素も多いため変なトラブルに巻き込まれることがある）
尚、Pythonにはバージョン2と3の2種類がありますが特にこだわりがなければ3をオススメします。
(詳細は以下記事にまとめています)

- [【Windows11】WinPythonをインストールする方法](./winpython-install-windows.md)

## 【方法4】WSL(Windows Subsystem for Linux)上でインストール

WindowsのWSLにインストールする方法もあります。
Linuxにしか対応していないライブラリを使うときは、この方法を使います。詳細は以下ページで解説します。

- [【WSL】Pythonをインストールして使う方法](./python-install-wsl.md)


## 関連ページ

[Python入門 サンプルと解説集](../index.md)


