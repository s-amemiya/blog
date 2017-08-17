title: Sequelizeを使う
date: 2017-08-17 08:12:10
tags: dev
---
## [Sequelize](http://docs.sequelizejs.com)

#### インストール

```
$ yarn add -D sequelize sequelize-cli
$ sequelize init
```

#### `./config/config.json` を修正する

#### モデル作成

```
$ sequelize model:create --name order --underscored --attributes user_id:string,price:string
```

#### DBに適用

```
$ sequelize db:migrate
```
