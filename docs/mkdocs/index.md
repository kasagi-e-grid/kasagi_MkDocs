# MkDocsについて

`作成者：笠木`

!!! info "**このドキュメントについて**"
    **MkDocsの使い方からデプロイまでのメモ**

## 使い方

* * *

1. <code style="color:#FF5370;">git clone https://github.com/kasagi-e-grid/kasagi_MkDocs</code>

2. <code style="color:#FF5370;">docker-compose up``` 又は ```docker-compose up -d</code>

3. [http://localhost:8000]()にアクセス

## 記法

* * *

> ### **Markdown記法**

調べてください

> ### **HTML記法**

調べてください

> ### **mkdocs-material記法**

!!! info "サンプル"
    サンプル

```
--- 書きかた ---
!!! info "サンプル"
    サンプル
```
他に使えるタイプ

| タイプ |
|:-----------|
| **info**       |
| **warning**     |
| **tip**      |
| **note**        |
| **danger**       |
| **question**     |

## デプロイ

* * *

※ github actionsで`main`にpushされた時点でデプロイされます。

1. <code style="color:#FF5370;">git push</code>


!!! note "**メモ**"

none