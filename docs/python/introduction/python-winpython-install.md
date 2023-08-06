# 【Windows】WinPythonを導入し、Python実行環境をUSBで持ち歩く方法

## WinPythonとは

WinPythonはポータブル化されたWindows環境向けのPythonパッケージです。
WinPythonの特徴は次の通りです。

1. Pythonの実行環境だけでなく、「主要なライブラリ群」や「便利な開発環境」も一括で導入してくれます。
    1. ※主要なライブラリ群・・・NumPy、Matplotlib、Pandas、SciPyなど（詳細はこちら）
    1. ※便利な開発環境・・・Spyder、Jupyter Notebookなど
1. ポータブル化されているため、インストール不要(レジストリを汚さない)。また、WinPythonの環境一式を丸ごとUSBに入れて持ち運び、他のPCで使える。
    1. ※職場やネットカフェ等の共有PCでもWinPythonをコピーしたUSBを差すだけで利用可能

公式サイトで配布されているインストーラを使ってPythonの実行環境を構築すると、主要なライブラリや開発環境のインストール作業も発生しますが、WinPythonではそれらをまとめて行えるため便利です。

## WinPythonのダウンロード

- 公式HP[https://sourceforge.net/projects/winpython/](https://sourceforge.net/projects/winpython/)にアクセスし、[Download]ボタンをクリックしてインストーラをダウンロードします。

- ダウンロードしたインストーラ(exeファイル)をダブルクリックして起動し、インストール先のフォルダを指定して「Extract」をクリックします。

- 指定したフォルダにインストールがされるので、終了するまで待ちます。

## 【実行方法①】WinPython Command Prompt

- 好きなテキストエディタ(VSCodeやメモ帳など)でPythonのプログラムを書き、拡張子を「.py」にしてファイルを保存します。

【例:test.py】

```
print('Hello world!')
```

③ 「WinPython Command Prompt.exe」を起動し、以下のコマンドを実行すると指定したPythonファイルを実行できます。

python Pythonファイルのパス

※Windows10では、Pythonファイルをコマンドプロンプトへドラッグ&ドロップすればパスが入力されるので楽です

実行例:test.pyを実行し、Hello world!と表示


【プログラム実行方法②】Spyder編

①「Spyder.exe」をダブルクリックして起動します。

②起動すると次のような画面が表示されます。
主に使うのは4つの赤枠部分です。


手順	説明
①	左側の赤枠部分にPythonのプログラムを書きます。
②	「実行」ボタンを押します。
③	実行結果がコンソールに表示されます。
④	プログラムの実行を途中で止めたい場合は「デバッグ中止」ボタンを押します。

③試しに赤枠部分に以下のプログラムを記述します。

print("Hello world!")

実行ボタンを押してコンソールに「Hello world!」と表示されれば成功です。

https://algorithm.joho.info/programming/python/spyder/

【プログラム実行方法③】Jupyter Notebook編

Jupyter Notebookとは、Webブラウザ上で動作するプログラムの対話型の実行環境です。
プログラムの実行、実行結果やメモの記録ができ、それらのデータを共有することもできます。
簡単な使用手順は次の通りです。

①「jupyter notebook.exe」をダブルクリックして起動します。

②しばらくすると、デフォルトのブラウザでJupyter Notebookの画面が表示されます。
画面右上の「New」→「Python 3」と選択すると、Python3の新しいノートブックを作成できます。



③ ln []: というセルの中にプログラムのソースコードを記述します。
セルを選択して「▶」ボタンを押すことで実行できます。（「Shift」+「Enter」キーでも実行可能）



④セルを選択してから「Code」を「Markdown」に変更すると、そのセルにMarkdown記述でメモを残すことができます。




⑤その他の主な昨日は次の通りです。


-	内容
①	保存
②	新しいセルの追加
③	セルの切り取り
④	セルのコピー
⑤	セルの貼り付け
⑥	セルの実行
⑦	実行停止
⑧	セルの書式

また、「Fille」→「Download As」からJSON形式、HTML形式、Latex形式など様々なファイル形式でノートブックを保存できます。

https://algorithm.joho.info/programming/jupyter-notebook-windows-linux/

https://algorithm.joho.info/programming/python/winpython-pre-run/

【WinPython】アンインストール手順

Pythonパッケージ「WinPython」はデフォルトでPortableです。
そのため、他のソフトのように「コントロールパネル」や「アプリの削除」画面からアインインストール作業を行う必要はありません。

WinPythonのインストール先のディレクトリを削除すればアンインストール完了となります。


## 関連ページ

[Python入門 サンプルと解説集](../index.md)




