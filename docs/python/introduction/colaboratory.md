# 【Google Colaboratory】WebブラウザでPythonを使う方法

## Google Colaboratoryとは

Google Colaboratoryとは、WebブラウザだけでPythonを実行できるGoogleのクラウドサービスです。
また、無料でGPU環境が使え、「TensorFlow」「Keras」「PyTorch」「Chainer」「OpenCV」等の外部モジュールが使えるため、機械学習も行えます。
クラウドサービスなので、Windows、Mac、LinuxなどのOSに依存せず、Chromeやfirefox等のブラウザさえ入れれば、Pythonプログラミングができます。
また、グラフィックスボードを備えたハイスペックなPCが不要で、開発環境構築の手間も省けるため、かなり便利なサービスです。

ただし、Google Colaboratoryでは以下の制約条件があります。

- 主な制約条件
    - ノートブックのサイズは最大20MB
    - ノートブックのセッションが切れてから90分経過すると、インスタンスの状態がすべてリセットされる【90分ルール】。
    - 新しいインスタンスを起動してから12時間経過すると、インスタンスの状態がすべてリセットされる【12時間ルール】。

また、Google Colaboratoryには無料版と有料版(Colab Pro、Colab Pro+)があります。
Pythonの練習をするなら無料版で十分ですが、それぞれの違いは以下表のとおりです。

項目|無料版|Colab Pro|Colab Pro+
--|--|--|--
月額利用料金|無料|1179円|5767円
GPU|自動割当|常に高性能なGPUが割当られる|常に高性能なGPUが割当られる
メモリ|普通(通常利用では十分)|大容量(大量のデータを扱える)|大容量(大量のデータを扱える)
使用時間|最長 12 時間|最長 24 時間|最長 24 時間
バックグラウンド実行|✕|✕|○


## ノートブックを作成してPythonを実行

- WebブラウザでGoogleアカウントにログインし、[https://colab.research.google.com/?hl=ja](https://colab.research.google.com/?hl=ja)にアクセスします。

- [ノートブックを新規作成] をクリックします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vT9EDRIaFfTajDnoxZxvQ39RnwBtiANefxx8NtRBapyIZuw8NP91Si0M4e4MhG52VFTWkzAwdTKk63w/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

- セルにプログラムを記述します。 [▶]ボタンをクリックします。すると、セルの下に実行結果が表示されます。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSEN79GcnR-DJN91K2Q61ILm1BejzdqSDgJxrRz6sQdZVKLzTIUagSv9vEq_6H2QTTgSq7Lc5qnhefY/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## ノートブックを保存、名前の変更

- 上部メニューから[ファイル]→[保存]をクリックして、作成したノートブックを保存します。

- 保存したノートブックの場所を開きたい場合、 上部メニューから[ファイル]→[ドライブを探す]をクリックします。

- ファイル名(ノートブックの名前)を変更したい場合、上部メニューから[ファイル]→[名前の変更]をクリックします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSOzzPbhg6AMX6aJ5-vzfIvX9UYc4IgStwe5lkTwDW1L4Tm2IiFNYWWne4QejSy0T3xNVqY2ATtJ12P/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

- Googleドライブ上で直接ファイル名を編集したり、移動することもできます。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vR9MwMcq9cgpA5hSXHtcyH5Mb3Gk8pooda6a1ZRs4s0xNMqLjCLlpMTPXbpLnu92Ws7yQ_dhWLsNgON/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## GPUの利用設定

- ノートブック画面上部から[ランタイム] → [ランタイムのタイプを変更]をクリックします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTxs2IJpeTemCz91cVRbGpUHPui_CT3ggo4u3GmTDZ1tDkNz--Hve8dTpTkFFV23G48WKr7j8QSiLsw/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>


- [ハードウェアアクセラレータ]の[GPU]で、使用したいGPUの種類を選択して保存します。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQikdE-wqtqIXKd6-UCrcb8WylJUcj2XXVdyXzTEFtWb6BqeZ0tOu2fqZRB8CRz9Rkie9cZVH2CHfMS/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## Googleドライブ上のファイルを読み込む

- 左端のフォルダアイコンをクリックします。

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRkSUXQ6ktMVbn0XS_bqgFzktmPDXyJOB6sDAtGr57ccNDYXmEZkFBgUCRzqFGWea5C_rPzmd7wWgB4/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

- 「Googleドライブに接続」をクリックします。Googleアカウントのログイン画面が出てきたらログインします。
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRj5_8axLBkcg4LVePwojCVpuGmkz3hQmspEH5BAgFA5TlghVBYJyJmLLdp_a8CyXijQ2-lboqr3XWw/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

- Googleドライブがマウントされ、「Drive」→「MyDrive」を展開すると、Googleドライブにアクセスできるようになります。
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSDzvyQ-H1mweHxnukvYc7zKGm5p800CBV0r1lDjxS7ctz7XG5EZzh2LJM4nrLIRPsLQOi6_iOV1-jp/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## ファイルのアップロード

- セルに下記のコードを書いて実行します。

```
from google.colab import files
uploaded = files.upload()
```
- 出力画面上にアップロード用のボタン[ファイル選択]が表示されます。それをクリックすることでファイルをアップロードできます。


## 外部モジュールの利用


