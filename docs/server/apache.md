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

1. <code style="color:#FF5370;">systemctl restart httpd</code>

2. <code style="color:#FF5370;">touch [RailsRoot]/tmp/restart.txt</code>

```tmp/restart.txt```　←　Passenger はこのファイルのタイムスタンプを見ることで再起動を判断します。

## 動作確認

* * *

1. <code style="color:#FF5370;">passenger-status</code>

2. <code style="color:#FF5370;">systemctl status httpd</code>

3. ```/var/httpd/logs/access.log```を確認する

4. Railsログを確認する

* * *
<br>

!!! note "**メモ**"

> #### 関連ポート

- 80

- 443