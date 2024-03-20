# 使い方


以下のコマンドを実行する
```
docker compose build
docker compose up -d
```

多分すぐ使えるはず?

# インストールされてるやつ
* vue:3.4
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

# 参考にしたサイト
* [【Vue3/Docker環境構築】Vue.js概要と起動の仕組み](https://reisuta.com/vue3-init/)
* [【Docker】バインドマウントによる上書きに要注意](https://zenn.dev/usma11dia0/articles/dockerfile_run_npm_not_working)

# これをもとに作った記事
[dockerでvueの環境構築するときにnode_modulesディレクトリで躓いた話](https://qiita.com/hideya670/items/2e31ef2bab3d897b3b67)