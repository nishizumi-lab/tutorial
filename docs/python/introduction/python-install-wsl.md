## 【WSL】Pythonをインストールして使う方法

## WSLとは

WSL（Windows Subsystem for Linux）とは、Windows10・11上でLinuxを実行できる機能です。
Microsoft Store経由でアプリのようにUbuntuやDebian等のLinuxのディストリビューションを利用できます。
WSL2の有効化とUbutnuのインストール方法については以下ページで紹介しています。

- [WSL2を有効化してUbuntuをインストールする方法」](../../windows/system/wsl-ubuntu.md)

今回は、上記ページのWSL2の有効化とUbutnuのインストールが完了している前提で、Pythonをインストールして実行する方法を紹介します。

## Pythonの実行

- Windows上で次のような簡単なPythonスクリプトファイルを作成します。
（ファイル名はsample.pyなどにします）

```
print('Excalibur')
```

- 作成したPythonスクリプトファイル（sample.py）を以下のディレクトリにコピーします。

```
C:\Users\＜Windowsのユーザー名＞\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState\rootfs\home\＜Ubuntuのユーザー名＞
```

※上記のディレクトリは、WSL上で実行するUbuntuのルートディレクトリ

- Ubuntuを起動し、ターミナルで以下のコマンドを実行します。

```
$sudo python sample.py
```

- 「Excalibur」がターミナルに表示されたら成功です。
※「python: can't open file 'sample.py': [Errno 13] Permission denied」というエラーが出た場合は下記事を参考にファイルの権限を変更するか、次のようにスーパーユーザーで実行すれば解消されます。

- [【WSL】Pythonが実行できないエラー対策「can't open file 'sample.py': [Errno 13] Permission denied」](./wsl-ubuntu-error-python-cant-open-file.md)


## 関連ページ

[Python入門 サンプルと解説集](../index.md)


