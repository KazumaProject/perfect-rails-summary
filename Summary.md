# パーフェクト Ruby on Rails 

Ruby : 2.6.6
Rails: 6.0.3

## rails command

```
rails -v

rails _<RAILS_VERSION>_ -v

rails _6.0.3_ new hello_rails
```

## rake file

```
desc 'Hello, Rake Task'
task :hello do
  puts 'Hello, Rake!'
end
```
```
rake -T

rake -f <FILE_NAME>

## 実行するコマンド
rake hello
```

- decs : 説明文

- task ~ : 実行する内容 

## bundle

Ruby 2.5 から Ruby 本体に組み込まれた

| コマンド    | 概要 |
| -------- | ------- |
| bundle install| Gemfile(.lock) に書かれている gem パッケージをインストールする |
| bundle update [ライブラリ名] | インストール済みの gem パッケージのバージョンを更新する|
| bundle list |　インストール済みの gem パッケージの一覧を表示する|
| bundle init | Gemfile を生成する |
| bundle exec [コマンド] | Bundler でインストールされている gem パッケージを使用してコマンドを実行する|

```Gemfile
# frozen_string_literal: true

source "https://rubygems.org"

git_source(:github) {
  |repo_name| "https://github.com/#{repo_name}"
}

gem "rails"

```

## Rails の思想

- Coc (Convention over Configuration)

- DRY (Don't Repeat Yourself)

- REST

- 自動テスト

### Coc

- データベースのテーブル名はモデル名の複数形にする

i.e. Employee model -> employees table name

- `/employees` という URL は社員の一覧を返す

- 社員 ID:1 の社員情報を表す URL は `/employees/1`

## rails のディレクトリ

| ファイル・ディレクトリ | 概要 |
| -------- | ------- |
| .ruby_version| rbenv などを使用している場合、このファイルに記載されたバージョンの Ruby を使用する |
| Gemfile [ライブラリ名] |  プロジェクトで使用する gem ファイルを定義したファイル |
| Gemfile .lock | Gemfile の依存関係を解決した結果を保存する |
| app/ | 主なアプリケーションコードを記載するディレクトリ |
| bin/ | Rails アプリケーションを開発するために利用する実行コマンドを格納しているディレクトリ|
| config/ | アプリケーションの動作に関する設定ファイルを格納するディレクトリ|
| db/ | DB に関する設定を格納するディレクトリ |
| lib/ | Rake タスクなどアプリケーションから独立したコードを格納するディレクトリ |
| public/| 静的コンテンツを配置するディレクトリ |
| test/ | テストに関するソースコードをまとめるディレクトり |
