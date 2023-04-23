# GitHub PagesのみでWebサイトを簡単に構築する方法

## GitHub Pages

GitHub Pagesは、GitHubにアップロードしたWebページのコンテンツ(HTML、CSS、Javascript、画像ファイル等)をWebサイトとして公開できる機能です。

## 静的サイトジェネレーター

静的サイトジェネレーターは、Webページのコンテンツ(HTML、CSS、Javascript、画像ファイル等)を生成するソフトウェアです。
GitHub Pagesと組合せる場合、MarkdownファイルをHTMLに変換できる静的サイトジェネレーターを用いるのが一般的です。
静的サイトジェネレーターは多種多様ですが、有名なものに「Jekyll」「Hugo」などがあります。

## GitHub Pages + Jekyll

静的サイトジェネレーターの1つで、2008年にリリースされた歴史あるものです。
Ruby製で日本語の公式ドキュメントがあります。
GitHubにもJekyllが組み込まれているため、利用者がローカル環境にJekyllをインストールしなくても、Markdownファイルを編集してGithubのブランチへcommitとpushをすれば、GitHubがHTMLファイルに変換し、自動でWebサイトを生成してくれます。

GitHub上のJekyllを用いる場合は、一部のプラグインしか使用することができないため、サポートされていないプラグインを使いたい場合は、ローカル環境上にJekyllを入れてビルドしてから、GitHubにcommitする必要があります。

ただし、その場合はMarkdownファイルの編集だけで済まなくなるため、利便性がかなり下がります。

