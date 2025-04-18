# Apache + Passenger 構成

`作成者：笠木`

!!! info "**このドキュメントについて**"
    **Apache + Passengerで普段実行しているコマンドなどをまとめたものです。**

## Requestまでの流れ

* * *

```
[Client]
   ↓
[Apache (mod_passenger)]
   ↓
[Rails App]
```

## 再起動方法

* * *

1. ```systemctl restart httpd```

2. ```touch [RailsRoot]/tmp/restart.txt```

```tmp/restart.txt```　←　Passenger はこのファイルのタイムスタンプを見ることで再起動を判断します。

## 動作確認

* * *

1. ```passenger-status```

2. ```systemctl status httpd```

3. ```/var/httpd/logs/access.log```を確認する

4. Railsログを確認する

* * *
<br>

!!! note "**メモ**"

> #### 関連ポート

- 80

- 443