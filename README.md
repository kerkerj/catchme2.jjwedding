# catchme2

This backend server is written in Node.js with Redis.

node version v4.4.4

## 開發

### Docker (需有 docker toolchain, 包含 `docker`, `docker-machine`, `docker-compose`)

```
$ docker-compose build
$ docker-compose up
$ open http://{docker_machine_ip} # check by docker env default
```

### 一般

```
第一次使用: p.s. 需要 node v4.4.4, 以及 redis, `npm --version` 至少要 3.x

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

1. 有時間的話作個 benchmark

## 0521 update:

相關數據在 statics 裡，含測試的 t2.micro 共花費 8.10 USD

EC2 m3.medium *2 + EC2 t2.micro * 1
redis t2.micro

EC2	$5.85
ElastiCache	$2.16
DataTransfer	$0.05
S3	$0.04
Other Services	$0.00
Tax	$0.00
