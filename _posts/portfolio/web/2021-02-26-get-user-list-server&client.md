---
layout: post
title: Get User List Server & Client Web App
author: twozeronine
categories:
  - portfolio
  - web
tags: [HTML, CSS, javascript, react, nodejs, graphql, express, apollo]
date: 2021-02-19 18:18 +0800
---

<center>
<span style=
"font-size:170%;
font-weight:bold">
get user list server & client web app
</span>
</center>

---

# Server

> [PedroTech](https://youtu.be/Dr2dDWzThK8)의 실습 결과물

express로 만든서버입니다.

graphQL를 사용하여 Client 유저목록을 보냅니다.

서버는 Heroku에 배포하였습니다.

[깃허브 소스코드](https://github.com/twozeronine/get-user-list-server)

## Environments

- node.js@12.20.1
- express@4.17.1
- express-graphql@0.12.0
- graphql@15.5.0
- cors@2.8.5
- body-parser@1.19.0
- http-proxy-middleware@1.0.6

---

# Client

> [PedroTech](https://youtu.be/YyUWW04HwKY)의 실습 결과물

react , react-apollo/client , graphGL 을 사용하여 만든 client로
express로 만든 서버에서 user list를 가져옵니다.

Heroku에 배포된 서버가 약 10초후에 작동하므로 결과를 보려면 약간의 대기시간이 있습니다. (후에 Heroku가 아닌 다른 곳에 서버를 배포할 예정입니다.)

[결과물 링크](https://get-user-list.netlify.app/)

[깃허브 소스코드](https://github.com/twozeronine/get-user-list-client)

## Environments

- react-scripts@4.0.2
- graphql@15.5.0
- @apollo/client@3.3.11
