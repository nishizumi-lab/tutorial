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


## 外部モジュールのインストール

- Google Colaboratoryでも、外部モジュールをインストールするときはpipを使います。
ただし、ローカルマシンと少し異なり、pipの前に!を付けて実行します。

```
!pip install パッケージ名
```

- なお、Pythonでよく利用されている機械学習ライブラリや計算ライブラリ、グラフ描画ライブラリは大体がインストール済なので、インストール作業は不要です。インストール済かどうかの確認方法は次の節で紹介します。

## Google Colaboratoryに標準搭載されている外部モジュール

- セルで「!pip freeze」を実行すると、Google Colaboratoryに標準搭載されている外部モジュールの一覧表が表示されます。2023年8月4日現在確認したところ、以下のとおりでした。これらは、特にインストール作業で利用できるモジュールです。主要な機械学習ライブラリや計算ライブラリ、グラフ描画ライブラリは揃っています。

```
absl-py==1.4.0
aiohttp==3.8.5
aiosignal==1.3.1
alabaster==0.7.13
albumentations==1.2.1
altair==4.2.2
anyio==3.7.1
appdirs==1.4.4
argon2-cffi==21.3.0
argon2-cffi-bindings==21.2.0
array-record==0.4.0
arviz==0.15.1
astropy==5.2.2
astunparse==1.6.3
async-timeout==4.0.2
attrs==23.1.0
audioread==3.0.0
autograd==1.6.2
Babel==2.12.1
backcall==0.2.0
beautifulsoup4==4.11.2
bleach==6.0.0
blinker==1.4
blis==0.7.10
blosc2==2.0.0
bokeh==3.1.1
branca==0.6.0
build==0.10.0
CacheControl==0.13.1
cachetools==5.3.1
catalogue==2.0.9
certifi==2023.7.22
cffi==1.15.1
chardet==4.0.0
charset-normalizer==2.0.12
chex==0.1.7
click==8.1.6
click-plugins==1.1.1
cligj==0.7.2
cloudpickle==2.2.1
cmake==3.25.2
cmdstanpy==1.1.0
colorcet==3.0.1
colorlover==0.3.0
community==1.0.0b1
confection==0.1.0
cons==0.4.6
contextlib2==21.6.0
contourpy==1.1.0
convertdate==2.4.0
cryptography==3.4.8
cufflinks==0.17.3
cvxopt==1.3.1
cvxpy==1.3.2
cycler==0.11.0
cymem==2.0.7
Cython==0.29.36
dask==2022.12.1
datascience==0.17.6
db-dtypes==1.1.1
dbus-python==1.2.18
debugpy==1.6.6
decorator==4.4.2
defusedxml==0.7.1
distributed==2022.12.1
distro==1.7.0
dlib==19.24.2
dm-tree==0.1.8
docutils==0.18.1
dopamine-rl==4.0.6
duckdb==0.8.1
earthengine-api==0.1.361
easydict==1.10
ecos==2.0.12
editdistance==0.6.2
en-core-web-sm @ https://github.com/explosion/spacy-models/releases/download/en_core_web_sm-3.5.0/en_core_web_sm-3.5.0-py3-none-any.whl#sha256=0964370218b7e1672a30ac50d72cdc6b16f7c867496f1d60925691188f4d2510
entrypoints==0.4
ephem==4.1.4
et-xmlfile==1.1.0
etils==1.4.0
etuples==0.3.9
exceptiongroup==1.1.2
fastai==2.7.12
fastcore==1.5.29
fastdownload==0.0.7
fastjsonschema==2.18.0
fastprogress==1.0.3
fastrlock==0.8.1
filelock==3.12.2
Fiona==1.9.4.post1
firebase-admin==5.3.0
Flask==2.2.5
flatbuffers==23.5.26
flax==0.7.0
folium==0.14.0
fonttools==4.41.1
frozendict==2.3.8
frozenlist==1.4.0
fsspec==2023.6.0
future==0.18.3
gast==0.4.0
gcsfs==2023.6.0
GDAL==3.4.3
gdown==4.6.6
gensim==4.3.1
geographiclib==2.0
geopandas==0.13.2
geopy==2.3.0
gin-config==0.5.0
glob2==0.7
google==2.0.3
google-api-core==2.11.1
google-api-python-client==2.84.0
google-auth==2.17.3
google-auth-httplib2==0.1.0
google-auth-oauthlib==1.0.0
google-cloud-bigquery==3.10.0
google-cloud-bigquery-connection==1.12.1
google-cloud-bigquery-storage==2.22.0
google-cloud-core==2.3.3
google-cloud-datastore==2.15.2
google-cloud-firestore==2.11.1
google-cloud-functions==1.13.1
google-cloud-language==2.9.1
google-cloud-storage==2.8.0
google-cloud-translate==3.11.2
google-colab @ file:///colabtools/dist/google-colab-1.0.0.tar.gz#sha256=0885853d84f852df4da0d294de7c7d02c701dd982d3280a456c3b4a12dc5e859
google-crc32c==1.5.0
google-pasta==0.2.0
google-resumable-media==2.5.0
googleapis-common-protos==1.59.1
googledrivedownloader==0.4
graphviz==0.20.1
greenlet==2.0.2
grpc-google-iam-v1==0.12.6
grpcio==1.56.2
grpcio-status==1.48.2
gspread==3.4.2
gspread-dataframe==3.3.1
gym==0.25.2
gym-notices==0.0.8
h5netcdf==1.2.0
h5py==3.8.0
holidays==0.29
holoviews==1.15.4
html5lib==1.1
httpimport==1.3.1
httplib2==0.21.0
humanize==4.6.0
hyperopt==0.2.7
idna==3.4
imageio==2.25.1
imageio-ffmpeg==0.4.8
imagesize==1.4.1
imbalanced-learn==0.10.1
imgaug==0.4.0
importlib-metadata==4.6.4
importlib-resources==6.0.0
imutils==0.5.4
inflect==6.0.5
iniconfig==2.0.0
intel-openmp==2023.2.0
ipykernel==5.5.6
ipython==7.34.0
ipython-genutils==0.2.0
ipython-sql==0.4.1
ipywidgets==7.7.1
itsdangerous==2.1.2
jax==0.4.13
jaxlib @ https://storage.googleapis.com/jax-releases/cuda11/jaxlib-0.4.13+cuda11.cudnn86-cp310-cp310-manylinux2014_x86_64.whl#sha256=af30095a0adf342b837a0ed9607e13177ee66f4e654c031a383aa546cd21d815
jeepney==0.7.1
jieba==0.42.1
Jinja2==3.1.2
joblib==1.3.1
jsonpickle==3.0.1
jsonschema==4.3.3
jupyter-client==6.1.12
jupyter-console==6.1.0
jupyter-server==1.24.0
jupyter_core==5.3.1
jupyterlab-pygments==0.2.2
jupyterlab-widgets==3.0.8
kaggle==1.5.16
keras==2.12.0
keyring==23.5.0
kiwisolver==1.4.4
langcodes==3.3.0
launchpadlib==1.10.16
lazr.restfulclient==0.14.4
lazr.uri==1.0.6
lazy_loader==0.3
libclang==16.0.6
librosa==0.10.0.post2
lightgbm==3.3.5
linkify-it-py==2.0.2
lit==16.0.6
llvmlite==0.39.1
locket==1.0.0
logical-unification==0.4.6
LunarCalendar==0.0.9
lxml==4.9.3
Markdown==3.4.4
markdown-it-py==3.0.0
MarkupSafe==2.1.3
matplotlib==3.7.1
matplotlib-inline==0.1.6
matplotlib-venn==0.11.9
mdit-py-plugins==0.4.0
mdurl==0.1.2
miniKanren==1.0.3
missingno==0.5.2
mistune==0.8.4
mizani==0.8.1
mkl==2019.0
ml-dtypes==0.2.0
mlxtend==0.22.0
more-itertools==9.1.0
moviepy==1.0.3
mpmath==1.3.0
msgpack==1.0.5
multidict==6.0.4
multipledispatch==1.0.0
multitasking==0.0.11
murmurhash==1.0.9
music21==8.1.0
natsort==8.3.1
nbclient==0.8.0
nbconvert==6.5.4
nbformat==5.9.1
nest-asyncio==1.5.6
networkx==3.1
nibabel==4.0.2
nltk==3.8.1
notebook==6.4.8
numba==0.56.4
numexpr==2.8.4
numpy==1.22.4
oauth2client==4.1.3
oauthlib==3.2.2
opencv-contrib-python==4.7.0.72
opencv-python==4.7.0.72
opencv-python-headless==4.8.0.74
openpyxl==3.0.10
opt-einsum==3.3.0
optax==0.1.7
orbax-checkpoint==0.3.1
osqp==0.6.2.post8
packaging==23.1
palettable==3.3.3
pandas==1.5.3
pandas-datareader==0.10.0
pandas-gbq==0.17.9
pandocfilters==1.5.0
panel==1.2.1
param==1.13.0
parso==0.8.3
partd==1.4.0
pathlib==1.0.1
pathy==0.10.2
patsy==0.5.3
pexpect==4.8.0
pickleshare==0.7.5
Pillow==9.4.0
pip-tools==6.13.0
platformdirs==3.9.1
plotly==5.13.1
plotnine==0.10.1
pluggy==1.2.0
polars==0.17.3
pooch==1.6.0
portpicker==1.5.2
prefetch-generator==1.0.3
preshed==3.0.8
prettytable==0.7.2
proglog==0.1.10
progressbar2==4.2.0
prometheus-client==0.17.1
promise==2.3
prompt-toolkit==3.0.39
prophet==1.1.4
proto-plus==1.22.3
protobuf==3.20.3
psutil==5.9.5
psycopg2==2.9.6
ptyprocess==0.7.0
py-cpuinfo==9.0.0
py4j==0.10.9.7
pyarrow==9.0.0
pyasn1==0.5.0
pyasn1-modules==0.3.0
pycocotools==2.0.6
pycparser==2.21
pyct==0.5.0
pydantic==1.10.12
pydata-google-auth==1.8.1
pydot==1.4.2
pydot-ng==2.0.0
pydotplus==2.0.2
PyDrive==1.3.1
pyerfa==2.0.0.3
pygame==2.5.0
Pygments==2.14.0
PyGObject==3.42.1
PyJWT==2.3.0
pymc==5.1.2
PyMeeus==0.5.12
pymystem3==0.2.0
PyOpenGL==3.1.7
pyparsing==3.1.0
pyproj==3.6.0
pyproject_hooks==1.0.0
pyrsistent==0.19.3
PySocks==1.7.1
pytensor==2.10.1
pytest==7.2.2
python-apt==0.0.0
python-dateutil==2.8.2
python-louvain==0.16
python-slugify==8.0.1
python-utils==3.7.0
pytz==2022.7.1
pyviz-comms==2.3.2
PyWavelets==1.4.1
PyYAML==6.0.1
pyzmq==23.2.1
qdldl==0.1.7.post0
qudida==0.0.4
regex==2022.10.31
requests==2.27.1
requests-oauthlib==1.3.1
requirements-parser==0.5.0
rich==13.4.2
rpy2==3.4.2
rsa==4.9
scikit-image==0.19.3
scikit-learn==1.2.2
scipy==1.10.1
scs==3.2.3
seaborn==0.12.2
SecretStorage==3.3.1
Send2Trash==1.8.2
shapely==2.0.1
six==1.16.0
sklearn-pandas==2.2.0
smart-open==6.3.0
sniffio==1.3.0
snowballstemmer==2.2.0
sortedcontainers==2.4.0
soundfile==0.12.1
soupsieve==2.4.1
soxr==0.3.5
spacy==3.5.4
spacy-legacy==3.0.12
spacy-loggers==1.0.4
Sphinx==5.0.2
sphinxcontrib-applehelp==1.0.4
sphinxcontrib-devhelp==1.0.2
sphinxcontrib-htmlhelp==2.0.1
sphinxcontrib-jsmath==1.0.1
sphinxcontrib-qthelp==1.0.3
sphinxcontrib-serializinghtml==1.1.5
SQLAlchemy==2.0.19
sqlparse==0.4.4
srsly==2.4.7
statsmodels==0.13.5
sympy==1.11.1
tables==3.8.0
tabulate==0.9.0
tblib==2.0.0
tenacity==8.2.2
tensorboard==2.12.3
tensorboard-data-server==0.7.1
tensorflow==2.12.0
tensorflow-datasets==4.9.2
tensorflow-estimator==2.12.0
tensorflow-gcs-config==2.12.0
tensorflow-hub==0.14.0
tensorflow-io-gcs-filesystem==0.32.0
tensorflow-metadata==1.13.1
tensorflow-probability==0.20.1
tensorstore==0.1.40
termcolor==2.3.0
terminado==0.17.1
text-unidecode==1.3
textblob==0.17.1
tf-slim==1.1.0
thinc==8.1.10
threadpoolctl==3.2.0
tifffile==2023.7.18
tinycss2==1.2.1
toml==0.10.2
tomli==2.0.1
toolz==0.12.0
torch @ https://download.pytorch.org/whl/cu118/torch-2.0.1%2Bcu118-cp310-cp310-linux_x86_64.whl#sha256=a7a49d459bf4862f64f7bc1a68beccf8881c2fa9f3e0569608e16ba6f85ebf7b
torchaudio @ https://download.pytorch.org/whl/cu118/torchaudio-2.0.2%2Bcu118-cp310-cp310-linux_x86_64.whl#sha256=26692645ea061a005c57ec581a2d0425210ac6ba9f923edf11cc9b0ef3a111e9
torchdata==0.6.1
```

