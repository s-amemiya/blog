---
layout: post
title:  "heroku memo"
date:   2016-04-21 00:00:00 +0900
categories: nodejs, heroku
---
```
$ heroku config:set NPM_CONFIG_PRODUCTION=false
$ heroku config:set NODE_MODULES_CACHE=false
$ git commit -am 'disable node_modules cache' --allow-empty
$ git push heroku master
```
