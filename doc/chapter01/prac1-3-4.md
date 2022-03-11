### 1. リスト 1.7のhelloアクションを書き換え、「hello, world!」の代わりに「hola, mundo!」と表示されるようにしてみましょう。

application_controller.rbのhello worldを書き換える
保存してブラウザのページを更新したら表示が変わった

### 2.Railsでは「非ASCII文字」もサポートされています。「¡Hola, mundo!」にはスペイン語特有の逆さ感嘆符「¡」が含まれています (図 1.20)12 。「¡」文字をMacで表示するには、Optionキーを押しながら1キーを押します。この文字をコピーして自分のエディタに貼り付ける方が早いかもしれません。

コピペしたら表示してくれた

### 3. リスト 1.7のhelloアクションを参考にして、２つ目のアクションgoodbyeを追加しましょう。このアクションは、「goodbye, world!」というテキストを表示します。リスト 1.9のルーティングを編集して、ルートルーティングの割り当て先をhelloアクションからgoodbyeアクションに変更します (図 1.21)。

```ruby:application_controller.rb
class ApplicationController < ActionController::Base
  protect_from_forgery with: :exception

  def hello
    render html: "¡Hora, mundo!"
  end

  def goodbye
    render html: "goodbye, world!"
  end
end
```

```ruby:routes.rb
Rails.application.routes.draw do
  root 'application#goodbye'
end
```
