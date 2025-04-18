# NFSについて

`作成者：笠木`

!!! info "**このドキュメントについて**"
    **マジカンのNFS（ネットワークファイルシステム）について**

## 前提情報

* * *

> NFSサーバ

- **133.242.18.191**　※rails3側のマジカンサーバー

> NFSクライアント

- **133.242.23.174**　※rails7側のマジカンサーバー

- **153.120.17.233**　※公開側

## NFSとは [#ドキュメント](https://docs.redhat.com/ja/documentation/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-nfs#s1-nfs-how)

* * *

**ネットワークを通じてファイルシステムを共有する際に使われる通信プロトコル。
主にUnix系OS同士のファイルシステム共有にはNFSが古くから使われており、
NFSサーバが公開したディレクトリをNFSクライアントがマウントすることで、
リモートファイルシステムをローカルファイルシステムと同様に扱うことが可能となる。**


## 接続手順

* * *

[参考記事](https://qiita.com/OPySPGcLYpJE0Tc/items/e3602d88d0d6eb02f5ee)

> ### NFSサーバ側

1. **NFSの公開ディレクトリを確認**　```cat /etc/exports```　←※ NFSクライアントに対するディレクトリ許可の記述があるか

2. **(※必要に応じて)**　```systemctl start nfs-server```

3. **(※必要に応じて)**　```systemctl enable nfs-server```

4. **NFSサーバのステータスを確認**　```systemctl status nfs-server```

5. **NFSサーバでエクスポートされているディレクトリを確認**　```showmount -e```

> ### NFSクライアント側

1. ```mount -t nfs {NFSクライアントIP}:///var/share/admintools/public/system /var/share/admintools/public/system```

2. **マウントされているか確認**　```df```


!!! note "**メモ**"

> #### UID, GIDについて

**UNIXではファイルのアクセス制御に「UID（ユーザーID）」と「GID（グループID）」を使います。**

**NFSもこの仕組みに基づいていて、NFSクライアントがファイルにアクセスするとき、**

**クライアント側のUID/GIDがそのままNFSサーバに送られ、サーバ側ではそのIDに基づいてアクセス権を判断します。**

[参考記事](https://atmarkit.itmedia.co.jp/fwin2k/productreview/sfu35-01/sfu35_01_03.html)

※実際のマジカンサーバーではGIDとUIDを統一しています。

