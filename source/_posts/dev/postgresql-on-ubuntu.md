title: postgresql-on-ubuntu
date: 2017-08-17 08:39:24
tags: dev
---
#### Ubuntu 16.04.2 組み込みposgresの設定

#### postgresユーザは、パスワードがない
```
postgres=# ALTER USER postgres PASSWORD '****'
```

#### psql: FATAL:  Peer authentication failed for user "postgres"の対応
```
$ sudo vi /etc/postgresql/9.1/main/pg_hba.conf
local   all             postgres                                peer
↓
local   all             postgres                                md5
```

#### port open
```
# vi /etc/postgresql/8.2/main/postgresql.conf
#listen_addresses = 'localhost'
↓
listen_addresses = '*'
$ sudo service postgresql restart
```

## 参考
[How To Install and Use PostgreSQL on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)

[Postgresql: password authentication failed for user “postgres”
](https://stackoverflow.com/questions/7695962/postgresql-password-authentication-failed-for-user-postgres)

[Getting error: Peer authentication failed for user “postgres”, when trying to get pgsql working with rails](https://stackoverflow.com/questions/18664074/getting-error-peer-authentication-failed-for-user-postgres-when-trying-to-ge)
