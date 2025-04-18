#　はじめに

このサイトでは、マジカン[133.242.23.174]で使用しているWebサーバーの構成・運用・トラブル対応等の

ナレッジをまとめています。

* * *

> ### Server

- [サーバー構成](/server/architecture/)
- [Apache設定](/server/apache/)

> ### deploy

- [デプロイ手順](/deploy/flow/)

> ### troubleshooting

- [トラブル対応](/troubleshooting/common_issues/)

> ### security

- [セキュリティ設定](/security/firewall/)

### MkDocsファイル構成

```
docs/
├── index.md                    ← はじめに
├── server/
│   ├── architecture.md         ← サーバー構成
│   ├── apache.md               ← Apache + Passenger 構成
│   ├── nfs.md                  ← NFSについて
│   |── backup.md               ← バックアップ・リストア
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