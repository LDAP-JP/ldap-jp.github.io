---
title: Web サイトのコンテンツ管理
layout: default
---
概要
----------------------------------------------------------------------

GitHub Pages (http://pages.github.com/) を利用しています。

  * https://github.com/LDAP-JP/ldap-jp.github.io

コンテンツ管理権限の取得
----------------------------------------------------------------------

  1. GitHub (https://GitHub.com/) のアカウントを取得し、
     自分の SSH 公開鍵を登録する。
  2. LDAP-JP スタッフメーリングリストで GitHub アカウント名を伝える。

コンテンツの保守
----------------------------------------------------------------------

リポジトリーのクローン (ローカルリポジトリー) を作成します。

``` console
$ mkdir ldap-jp
$ cd ldap-jp
$ git clone git@github.com:LDAP-JP/ldap-jp.github.io.git
$ cd ldap-jp.github.io
```

ローカルリポジトリーにリモートリポジトリーの更新を取り込みます (プル)。

``` console
$ git pull
…
```

ローカルリポジトリーでコンテンツを編集、確認します。
https://help.github.com/articles/github-flavored-markdown

``` console
$ vi index.md
… コンテンツを編集 …
```

Jekyll (ジキル) がインストールされている環境なら、ローカルで
Markdown ファイル (`\*.md`) から HTML ファイルへの変換と表示の確認が可能です。

変換対象 Markdown ファイルは、先頭に MarkYAML Front Matter (「---」〜「---」)
が付いているファイルだけ。
ローカル Web サーバーの URL は http://localhost:4000。

``` console
$ make
… Markdown ファイルから HTML ファイルを生成 …

$ make server
… ローカル Web サーバーを起動 …
```

ローカルリポジトリーに編集結果をコミットします。
コミットログメッセージは*日本語で OK* です。

``` console
$ git commit
…
```

編集〜ローカルリポジトリーへのコミットを必要なだけ繰り返します。

ローカルリポジトリーのコミットをリモートリポジトリーに送信します (プッシュ)。

``` console
$ git push
…
```

