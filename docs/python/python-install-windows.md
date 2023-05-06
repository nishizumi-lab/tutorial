# PythonをWindowsにインストールする方法(公式インストーラ、WinPython、Anaconda、WSLなど)

# はじめに

WindonsにPythonの開発環境を構築する方法は、「公式インストーラ」と「Pythonパッケージ」「WSL：Windows Subsystem for Linux」「Docker」を使う物など様々です。
基本的には、「公式インストーラ」がおすすめですが、Python初心者で、とにかく早く機械学習とか試したいという方には「WinPython」や「Anaconda(Miniconda)」などのPythonパッケージを使うのが手軽です。
Pythonパッケージは、Pythonだけでなく「主要な外部ライブラリ」や「統合開発環境」も一括導入できて楽だからです。公式配布インストーラだと、後から自分で外部ライブラリを入れていく必要があります。
ただし、Pythonパッケージ特有のトラブルとかもあるので、一長一短です。

また、Pythonにはバージョン2と3の2種類がありますが特にこだわりがなければバージョン3をオススメします。

## 公式インストーラー

ある程度Pythonに使い慣れてきたら、公式インストーラー＋VScodeで開発をすすめるのがおすすめ。
VScodeのPythonプラグインを使うことで効率よく中～大規模なプログラムを構築できます。
(詳細は以下記事にまとめています)

## Pythonパッケージ（WinPython or Anaconda）を用いる方法

「WinPython」でPythonを始めるのがおすすめ。
（Anacondaは高機能だが独自機能の要素も多いため変なトラブルに巻き込まれることがある）
尚、Pythonにはバージョン2と3の2種類がありますが特にこだわりがなければ3をオススメします。
(詳細は以下記事にまとめています)

https://algorithm.joho.info/programming/python/winpython/

https://algorithm.joho.info/programming/python/anaconda/



https://algorithm.joho.info/programming/python/vscode-debug-run/

## WSL

WindowsのWSLにインストールする方法もあります。
Linuxにしか対応していないライブラリを使うときは、この方法を使っています。
(詳細は以下記事にまとめています)


