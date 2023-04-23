# GitHub PagesのみでWebサイトを簡単に構築する方法

## GitHub Pages

GitHub Pagesは、GitHubにアップロードしたWebページのコンテンツ(HTML、CSS、Javascript、画像ファイル等)をWebサイトとして公開できる機能です。

## 静的サイトジェネレーター

静的サイトジェネレーターは、Webページのコンテンツ(HTML、CSS、Javascript、画像ファイル等)を生成するソフトウェアです。
GitHub Pagesと組合せる場合、MarkdownファイルをHTMLに変換できる静的サイトジェネレーターを用いるのが一般的です。
静的サイトジェネレーターは多種多様ですが、有名なものに「Jekyll」「Hugo」などがあります。

## Jekyll

Jekyllは、静的サイトジェネレーターの1つで、2008年にリリースされた歴史あるものです。
Ruby製で日本語の公式ドキュメントがあります。
GitHubにもJekyllが組み込まれているため、利用者がローカル環境にJekyllをインストールしなくても、Markdownファイルを編集してGithubのブランチへcommitとpushをすれば、GitHubがHTMLファイルに変換し、自動でWebサイトを生成してくれます。

GitHub上のJekyllを用いる場合は、一部のプラグインしか使用することができないため、サポートされていないプラグインを使いたい場合は、ローカル環境上にJekyllを入れてビルドしてから、GitHubにcommitする必要があります。

ただし、その場合はMarkdownファイルの編集だけで済まなくなるため、利便性がかなり下がります。

## ページの作成

- リポジトリを作成し、masterブランチに「docs/index.md」をcommit、pushします。

- 「Settings」ボタンをクリックし、「GitHub Pages」を開きます。

- 「docs folder」を選択して「Save」をクリックします。

- 上記URLにアクセスすると、Webページが表示されます。


## テーマを設定

● 「docsディレクトリ配下にJekyllの設定ファイル「_config.yml」を作成し、以下のように記載します。

```
theme: jekyll-theme-modernist
```

なお、Jekyll(GitHub Pages版)で利用できるテーマは以下ページに掲載されているもののみになります。

- [https://pages.github.com/themes/](https://pages.github.com/themes/)

## Jekyll(GitHub Pages版)のプラグインを設定

- Jekyll(GitHub Pages)で使えるプラグインは以下ページに掲載されています。
    - [https://pages.github.com/versions/](https://pages.github.com/versions/)
- 例えば、「Jemoji」といプラグインを使う場合は、「_config.yml」に以下のように追記して、commit・pushします。

```
plugins:
– jemoji
```

## 関連ページ



- [GitHub PagesとJekyllについて](https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll
)


