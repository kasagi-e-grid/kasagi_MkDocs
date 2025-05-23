# MkDocs セットアップ

## 手順
1. `git clone https://github.com/kasagi-e-grid/kasagi_MkDocs`
2. `docker-compose up`又は`docker-compose up -d`
3. [http://localhost:8000](http://localhost:8000)にアクセス

## mkdocs-material記法

- mkdocsのカスタム記法

```
--- 書きかた ---
!!! info "サンプル"
    サンプル
```

## デプロイ
※ github actionsでmainにpushされた時点でデプロイされます。