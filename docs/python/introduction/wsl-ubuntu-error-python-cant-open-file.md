# 【WSL】Pythonが実行できないエラー対策「can't open file 'sample.py': [Errno 13] Permission denied」

## [Errno 13] Permission denied エラー（Python実行時）

WSL(Windows Subsystem for Linux)でPython実行時に以下のようなエラーが出ることがあります。

```
python : can't open file 'sample.py': [Errno 13] Permission denied
```

これはPythonファイルの実行権限が付与されていないことが原因です。
ターミナルで以下のようなchmodコマンドを実行し、Pythonファイルの権限を変更してやることでエラーが解消されます。

```
$ chmod 400 sample.py
```