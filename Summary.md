# パーフェクト Ruby on Rails 

Ruby : 2.6.6
Rails: 6.0.3

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
