
# これは何？

TBW

# 初回セットアップ

```zsh
bundle install
```

## パスワード入力を省略できるようにするには

```zsh
$ bundle exec fastlane fastlane-credentials add --username yourappleid@example.com
Password: \*\*\*\*\*\*\*\*\*
Credential yourappleid@example.com:\*\*\*\*\*\*\*\* added to keychain.
```

詳細は <https://github.com/fastlane/fastlane/tree/master/credentials_manager> を参照

# 使い方

## インストールできるバージョンを調べる

```zsh
bundle exec xcversion list
```

## インストールする

```zsh
bundle exec xcversion install 12.5
```

# 仕組み

- 環境を汚さないため、Ruby Bundlerでxcode-install(xcversion)とそのディペンデンシを管理します。それだけです。

# メモ

- `bundle exec`について
  - `bundle exec`は明示的につけている
  - `bundle exec`をつけると若干早くなる可能性があるため。fastlaneがそのようなメッセージを出していた。
  - また`bundle exec`をつけると確実にbundler管理下のものが実行されるため
