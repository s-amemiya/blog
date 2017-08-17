title: settings-for-ip
date: 2017-08-17 13:42:21
tags:
---

#### 設定ファイルを開く
```
$ vi /etc/network/interfaces
```

#### 追記

```
# The primary network interface
auto eth0
iface eth0 inet static
    address 10.0.0.41
    netmask 255.255.255.0
    gateway 10.0.0.1
```

#### サービスの再起動
```
$ sudo service networking restart
```

#### 参考
[Configure Networking on Ubuntu](https://www.swiftstack.com/docs/install/configure_networking.html)
