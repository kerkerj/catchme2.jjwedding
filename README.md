# catchme2

This backend server is written in Node.js with Redis.

node version v4.4.3

```
第一次使用: p.s. 需要 node v4.4.3, 以及 redis, `npm --version` 至少要 3.x

$ npm install -g npm # 如果版本是 2.x 的話

$ cp config.yml.example config.yml

$ npm install

$ npm start

$ open http://localhost:5566/

$ npm run serve_statics # 只 serve html，方便開發 (嗎?)

開發時使用:

$ npm run dev # to start nodemon service to reload files

發佈時先 build:

$ npm run build # to build ES6 js

實際執行使用:

$ npm start
```

設定檔在 `config.yml`

TODO:

1. 邀請碼

2. 在進入遊戲與遊戲清單頁面時，前端要送 client user name or uid，以判斷是否讓他進入，否則讓他轉回 login 頁

3. 有時間的話作個 benchmark

4. server 放哪？
