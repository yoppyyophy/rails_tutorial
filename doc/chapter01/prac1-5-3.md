### 1. 1.3.4.1と同じ変更を行い、本番アプリでも「hola, mundo!」を表示できるようにしてください。

* `config/route.rb`のアクション名を`hello`にする
* `/app/controllers/application_controller.rb`の出力内容を`hola, mundo!`にする

### 2. 1.3.4.1と同様、ルートへのルーティングを変更してgoodbyeアクションの結果が表示されるようにしてください。またデプロイ時には、Git pushのmasterをあえて省略し、git push herokuでデプロイできることを確認してみてください。

* `config/route.rb`のアクション名を`goodbye`にする
* `git push heroku`でも確かにデプロイできた