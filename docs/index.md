#　はじめに

このサイトでは、マジカン[133.242.23.174]で使用しているWebサーバーの構成・運用・トラブル対応等の

ナレッジをまとめています。

* * *

> ### Server

- [サーバー構成](server/architecture.md)
- [Apache設定](server/apache.md)

> ### deploy

- [デプロイ手順](deploy/flow.md)

> ### troubleshooting

- [トラブル対応](troubleshooting/common_issues.md)

> ### security

- [セキュリティ設定](security/firewall.md)

### MkDocsファイル構成

```
docs/
├── index.md                    ← はじめに
├── server/
│   ├── architecture.md         ← サーバー構成
│   ├── apache.md               ← Apache + Passenger 構成
│   ├── nfs.md                  ← NFSについて
├── deploy/
│   ├── flow.md                 ← デプロイフロー
├── git/
│   ├── operation.md            ← Git運用
├── troubleshooting/
│   ├── logs.md                 ← ログの確認
|── security/
|   ├── firewall.md             ← ファイアウォール設定
|   └── ssh.md                  ← SSH接続・鍵管理
└── stylesheets/                ← CSS
```