# 使い方


以下のコマンドを実行する
```
docker compose build
docker compose up -d
```

# インストールされてるやつ
* vue router
* pinia
* vitest
* playwright
* eslint
* prettier
* vue devTools

# vite.config.jsの設定
以下の設定を追加
```
server: {
    // --hostと同義,とりあえずこれでコンテナの外から通信できると思う?
    host: true,
    // 立ち上げる際のポートを変更できる。
    port: 5173
  }
```
細かいことは略すが､`yarn dev --host`,npmの場合は`npm run dev --host`と書かないとホスト側からアクセスできない｡  
`host: true`にすることで,`--host`がいらなくなる  
`port:5173`でポートを固定ができる｡何かあったら個々をいじることでポートを変更ができる｡