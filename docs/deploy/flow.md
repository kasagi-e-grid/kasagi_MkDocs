# デプロイフロー

`作成者：笠木`

!!! info "**このドキュメントについて**"
    **マジカンのデプロイ手順をまとめたものです。**

## デプロイ

* * *

1. **SSHアクセス**　```ssh -p 23422 -i 秘密鍵 majisemi@133.242.49.167```

2. **プロジェクトファイルに移動**　```cd /var/share/admintools```

3. ```git fetch```

4. ```git pull```

5. **(※必要に応じて)**　```bundle install```

6. **(※必要に応じて)**　```bundle exec rails assets:precompile```

7. **Apacheの再起動**　```systemctl restart httpd```

!!! note "**メモ**"

none
