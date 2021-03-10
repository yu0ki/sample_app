# レポジトリsample_appについての説明

このレポジトリはRuby on Railsの使用方法を学ぶために作成した練習用アプリケーションである。
タイトルと本文を１セットにしたレコード（投稿）をデータベースに保存し、それらを新規作成、表示、編集できるようにしている。

# 各フォルダ・ファイルについての説明
このウェブアプリケーションはMVC(Model View Controller)モデルで構成されていて、役割ごとにディレクトリを分けて保存されている。
主要なディレクトリについてどのようなファイルが含まれるのかメモしておく。


## config/routes.rb
ルーティングを行う部分。ユーザーがあるURLに、あるHTTPリクエストを伴ってアクセスしたとき、
どのコントローラーのどのアクションを実行するかを決定する。

## app/controllers
MVCモデルのCの部分。各種コントローラーが含まれている。コントローラーには、アクションの定義が書かれている。

## app/views
MVCモデルのVの部分。.html.erb形式のファイルによって、Rubyスクリプトを埋め込んだHTMLファイルを実現している。
これによって、ウェブアプリケーション内で表示されるページの内容を決めている。

## app/models
MVCモデルのMの部分。コントローラーで定義されたアクションのうち、データベースへのアクセスを必要とするものがあれば、
この機能を介してデータベースの情報を入手したり、データの追加・更新を行ったりする。

## app/models/list.rb
gemであるrefileが指定のカラムにアクセスするために、attachmentメソッドを追加する

## /Gemfile
どのパッケージやライブラリ（gem）を使用するかを記述するファイル。

## config/initializers/application_controller_renderer.rb
画像投稿を行う時に"Refile.secret_key"を求められるエラーが出たので、"Refile.secret_key"をここに登録している。

## app/views/layouts/application.html.erb
全てのページに共通するレイアウトを記述するファイル。ヘッダーやフッターなどを記述しておくとよい。

## app/assets/stylesheets/application.css
application.html,erbと紐づけられたCSSファイル。




