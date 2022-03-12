### 1. heroku helpコマンドを実行し、Herokuコマンドの一覧を表示してみてください。Herokuアプリのログを表示するコマンドはどれですか?

```bash
$ heroku help
CLI to interact with Heroku

VERSION
  heroku/7.59.4 linux-x64 node-v12.21.0

USAGE
  $ heroku [COMMAND]

COMMANDS
  access          manage user access to apps
  addons          tools and services for developing, extending, and
                  operating your app
  apps            manage apps on Heroku
  auth            check 2fa status
  authorizations  OAuth authorizations
  autocomplete    display autocomplete installation instructions
  buildpacks      scripts used to compile apps
  certs           a topic for the ssl plugin
  ci              run an application test suite on Heroku
  clients         OAuth clients on the platform
  config          environment variables of apps
  container       Use containers to build and deploy Heroku apps
  domains         custom domains for apps
  drains          forward logs to syslog or HTTPS
  features        add/remove app features
  git             manage local git repository for app
  help            display help for heroku
  keys            add/remove account ssh keys
  labs            add/remove experimental features
  local           run Heroku app locally
  logs            display recent log output
  maintenance     enable/disable access to app
  members         manage organization members
  notifications   display notifications
  orgs            manage organizations
  pg              manage postgresql databases
  pipelines       manage pipelines
  plugins         list installed plugins
  ps              Client tools for Heroku Exec
  psql            open a psql shell to the database
  redis           manage heroku redis instances
  regions         list available regions for deployment
  releases        display the releases for an app
  reviewapps      manage reviewapps in pipelines
  run             run a one-off process inside a Heroku dyno
  sessions        OAuth sessions
  spaces          manage heroku private spaces
  status          status of the Heroku platform
  teams           manage teams
  update          update the Heroku CLI
  webhooks        list webhooks on an app
  ```

  `logs`かな？

### 2. 上の演習で見つけたコマンドを使って、Herokuアプリの最近のログ (log) を調べてみましょう。直近に発生したイベントは何でしたか? (このログを調べるコマンドを覚えておくと、本番環境の不具合を見つけるときに役立ちます)

```bash
2022-03-12T07:50:59.568219+00:00 heroku[web.1]: Idling
2022-03-12T07:50:59.636101+00:00 heroku[web.1]: State changed from up to down
2022-03-12T07:51:02.643953+00:00 heroku[web.1]: Stopping all processes with SIGTERM
2022-03-12T07:51:02.756953+00:00 app[web.1]: - Gracefully stopping, waiting for requests to finish
2022-03-12T07:51:02.756998+00:00 app[web.1]: === puma shutdown: 2022-03-12 07:51:02 +0000 ===
2022-03-12T07:51:02.757002+00:00 app[web.1]: - Goodbye!
2022-03-12T07:51:02.757029+00:00 app[web.1]: Exiting
2022-03-12T07:51:02.890225+00:00 heroku[web.1]: Process exited with status 0
```

`heroku rename`したからダウンしたみたい