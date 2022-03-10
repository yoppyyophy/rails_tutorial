https://railstutorial.jp/chapters/beginning?version=5.1#cha-beginning

演習1.1.2を実施

クラウド上のIDEを使う。（WSL上で環境構築する気マンマンだった…）AWSでCloud9の環境を作成。

インデントをスペース2に変更。

Railsをインストール。

最初のアプリを作ってみる。
→hello_appを作成。

`~> 4.0.0` は「4.0.0より大きく、4.1より小さい」の意味。

バージョンをチュートリアルのものと揃えるため、Gemfileの中身を置き換える。

`bundle install`時にエラー

```bash
$ bundle install
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/.
You have requested:
  spring = 2.0.2

The bundle currently has spring locked at 2.1.1.
Try running `bundle update spring`

If you are updating multiple gems in your Gemfile at once,
try passing them all to `bundle update`
```

指示通り`bundle update spring`してみる

```bash
$ bundle update spring
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/.
Resolving dependencies...
Bundler could not find compatible versions for gem "activesupport":
  In snapshot (Gemfile.lock):
    activesupport (= 5.1.7)

  In Gemfile:
    rails (= 5.1.6) was resolved to 5.1.6, which depends on
      activesupport (= 5.1.6)

    coffee-rails (= 4.2.2) was resolved to 4.2.2, which depends on
      railties (>= 4.0.0) was resolved to 5.1.7, which depends on
        activesupport (= 5.1.7)

Running `bundle update` will rebuild your snapshot from scratch, using only
the gems in your Gemfile, which may resolve the conflict.
```

またエラー…`bundle update`で解消するかな？
その後もう一度`bundle install`してみる。→いけたみたい
