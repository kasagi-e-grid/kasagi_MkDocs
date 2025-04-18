# デプロイフロー

`作成者：笠木`

!!! info "**このドキュメントについて**"
    **マジカンのデプロイ手順をまとめたものです。**

## デプロイ

* * *

1. **SSHアクセス**　<code style="color:#FF5370;">ssh -p 23422 -i 秘密鍵 majisemi@133.242.49.167</code>

2. **プロジェクトファイルに移動**　<code style="color:#FF5370;">cd /var/share/admintools</code>

3. <code style="color:#FF5370;">git fetch</code>

4. <code style="color:#FF5370;">git pull</code>

5. **(※必要に応じて)**　<code style="color:#FF5370;">bundle install</code>

6. **(※必要に応じて)**　<code style="color:#FF5370;">bundle exec rails assets:precompile</code>

7. **Apacheの再起動**　<code style="color:#FF5370;">systemctl restart httpd</code>

!!! note "**メモ**"

none
