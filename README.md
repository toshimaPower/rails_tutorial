# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


# Ruby on Rails チュートリアルのサンプルアプリケーション

これは、次の教材で作られたサンプルアプリケーションです。   
[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
[Michael Hartl](http://www.michaelhartl.com/) 著

## ライセンス

[Ruby on Rails チュートリアル](https://railstutorial.jp/)内にある
ソースコードはMITライセンスとBeerwareライセンスのもとで公開されています。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

## 使い方

このアプリケーションを動かす場合は、まずはリポジトリを手元にクローンしてください。
その後、次のコマンドで必要になる RubyGems をインストールします。

```
$ bundle install --without production
```

その後、データベースへのマイグレーションを実行します。

```
$ rails db:migrate
```

最後に、テストを実行してうまく動いているかどうか確認してください。

```
$ rails test
```

テストが無事に通ったら、Railsサーバーを立ち上げる準備が整っているはずです。

```
$ rails server
```

詳しくは、[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
を参考にしてください。


$ rails generate controller StaticPages home help
$ rails destroy  controller StaticPages home help

なお第6章でも、次のようにモデルを自動生成する方法を紹介します。

$ rails generate model User name:string email:string
モデルの自動生成についても、同様の方法で元に戻すことができます。

$ rails destroy model User


また、第2章でも簡単に紹介しましたが、マイグレーションの変更を元に戻す方法も用意されています。詳細は第6章で説明しますが、簡単に紹介すると、まずdb:migrateでデータベースのマイグレーションを変更します。

$ rails db:migrate
元に戻したいときは、db:rollbackで1つ前の状態に戻します。

$ rails db:rollback
最初の状態に戻したいときは、VERSION=0オプションを使います。

$ rails db:migrate VERSION=0

