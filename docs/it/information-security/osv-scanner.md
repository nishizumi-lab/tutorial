## OSV-Scannerとは

OSV-Scannerは、Googleがオープンソースで開発しているGo製の脆弱性スキャンツールです。
プロジェクトで使用しているロックファイル(「Gemfile.lock」「packege-lock.json」など)に記述されたライブラリ群に存在する脆弱性をOSVデータベースと照合して検出します。

## OSV-Scannerのインストール

- Macでは、ターミナルを以下で実行してインストールできます。

```
brew install osv-scanner
```

- Linuxでは、ターミナルを以下で実行してインストールできます(先にgoのインストールが必要)。

```
sudo apt install -y golang-go
go install github.com/google/osv-scanner/cmd/osv-scanner@v1
```

## OSV-Scannerの使い方


以下のように、osv-scannerで脆弱性を調べたいロックファイルを指定して実行します。

```
osv-scanner -L ロックファイルのパス
```

【使用例】
```
osv-scanner -L package-lock.json
```

