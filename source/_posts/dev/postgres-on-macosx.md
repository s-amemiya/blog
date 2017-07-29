title: postgres-on-macosx
date: 2017-07-29 16:34:12
tags: [dev, postgresql]
---
MacOSXに開発用の`postgresql`を構築したときのメモ。

#### インストール
```
$ brew install postgresql
```

#### サービスの起動とOS起動時の設定

```
$ pg_ctl -D /usr/local/var/postgres start && brew $ services start postgresql
```

#### postgresロールがなかったのでつくる
```
$ /usr/local/Cellar/postgresql/9.6.3/bin/createuser -s postgres
$ psql postgres
postgres=# \du
                                   List of roles
 Role name |                         Attributes                         | Member of
-----------+------------------------------------------------------------+-----------
 postgres  | Superuser, Create role, Create DB                          | {}
 shinya    | Superuser, Create role, Create DB, Replication, Bypass RLS | {}
```

#### DB作成
```
$ /usr/local/Cellar/postgresql/9.6.3/bin/createdb rslite -U postgres
```

#### 参考ページ
[Getting Started with PostgreSQL on Mac OSX](https://www.codementor.io/devops/tutorial/getting-started-postgresql-server-mac-osx)

[psql: FATAL: role “postgres” does not exist
](https://stackoverflow.com/questions/15301826/psql-fatal-role-postgres-does-not-exist)
