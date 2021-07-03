---
layout: post
title: Post-blog-Client & Server
author: twozeronine
categories:
  - portfolio
  - web
tags: [HTML, CSS, javascript, react, koa, mogoDB, redux]
date: 2021-03-15 20:18 +0800
last_modified_at: 2021-03-30 01:08:25 +0800
---

<center>
<span style=
"font-size:170%;
font-weight:bold">
post-blog-client & server
</span>
</center>

---

# Client

간단한 포스트를 작성, 읽기, 수정, 삭제 등 할 수 있는 CRUD 블로그 웹 앱의 client입니다.

[깃허브 소스코드](https://github.com/twozeronine/post-blog-client)

## 스타일

styled-components를 사용하여 스타일을 적용하였고

## 라우터

react-router-dom를 사용하여  
LoginPage, RegisterPage, WritePage, PostPage, PostListPage 총 5개의 페이지를 구현하였습니다.

서버에서 제공하는 HTTP 헤더에 'last-page'를 받아와서 PostListPage에서 페이지네이션 기능을 구현하였습니다.

## 상태관리

React-redux를 사용하여 상태관리를 합니다  
Ducks 패턴으로 redux관련 파일은 모두 modules에 작성했습니다.

Container-Presenter 디자인 패턴으로 데이터 처리와 데이터 출력을 하는 파일들을 나눠서 작성하였습니다.

Container Components는 containers  
Presentational Components는 components  
폴더에서 확인할 수 있습니다.

## API 서버와 연동

axios를 사용하여 API를 호출합니다.

Redux-saga 미들웨어를 사용하여 API 요청과 같은 비동기적 작업을 관리합니다.

## 배포

배포하는 웹서버를 nginx를 사용하여 새로 구현하지 않고 API를 제공하는 [post-blog-server](https://github.com/twozeronine/post-blog-server) 서버에서 koa-static을 사용하여 정적 파일을 제공하도록 통합해서 구현하였습니다.

그후에 Docker를 사용하여 빌드된 클라이언트와 서버를 이미지로 만들었고

Google Cloud Run에 빌드된 이미지를 올려서 배포하였습니다.

> [Young-blog](https://blog-axhvl5dnbq-an.a.run.app/) 배포된 사이트입니다.

---

## page

### 회원가입

"/register"

### 로그인

"/login"

### 포스트 작성

"/write"

### 포스트 목록 조회

"/" ,"/?tag" , "/@:username"

### 포스트 조회

"/@:username/:postId"

---

## Environments

- axios@0.21.1
- immer@9.0.1
- qs@6.10.1
- quill@1.3.7
- react@17.0.1
- react-dom@17.0.1
- react-helmet-async@1.0.9
- react-redux@7.2.2
- react-router-dom@5.2.0
- react-scripts@4.0.3
- redux@4.0.5
- redux-actions@2.6.5
- redux-devtools-extension@2.13.9
- redux-saga@1.1.3
- styled-components@5.2.1

---

# Server

간단한 포스트를 작성, 읽기, 수정, 삭제 등 할 수 있는 CRUD 블로그 웹 앱의 server입니다.

[깃허브 소스코드](https://github.com/twozeronine/post-blog-server)

## REST API

Node.js의 koa 프레임워크를 사용하여 REST API를 구현하였습니다.

## 포스트 관리

Joi 라이브러리를 사용하여 클라이언트에서 작성된 포스트를 검증하여 올바른 요청이면 데이터베이스에 데이터를 저장하고 그렇지 않으면 오류메세지를 보내도록 구현하였습니다.

sanitize-html 라이브러리를 사용하여 클라이언트에서 글쓰기를 할 때 악성코드 삽입 방지를 위하여 HTML을 필터링하였습니다.

## 유저 관리

jsonwebtoken 라이브러리를 사용하여 JSON 토큰을 발급하고 쿠키에 유저정보를 저장하여 회원가입 , 로그인 , 로그아웃 기능에 필요한 회원 인증 시스템을 구현하였습니다.

## 데이터 베이스

mongoDB Atlas를 사용하여 서버와 데이터베이스를 연결하였습니다.

mongoDB Atlas는 mongodb에서 제공하는 클라우드 데이터베이스로 환경변수에 저장된 URI를 통해 연동했습니다.

> 환경변수 파일 .env는 보안을 위해 git에 올리지않았습니다.

## 배포

※ 3 / 30 추가내용  
koa-static 라이브러리를 사용하여 보통 클라이언트를 배포할때 사용하는 nginx 서버를 따로 구현하지않고

현재 이 API서버에 정적인 페이지를 제공하게끔 통합하여 구현 하였습니다.

Docker를 사용하여 빌드된 클라이언트와 서버를 이미지로 만들었고

Google Cloud Run에 빌드된 이미지를 올려서 배포하였습니다.

> [Young-blog](https://blog-axhvl5dnbq-an.a.run.app/) 배포된 사이트입니다.

---

## posts API

### 포스트 등록하기

- POST /api/posts

```json
/* Request body */
{
  "title": "제목",
  "body": "내용",
  "tags": ["태그1", "태그2"]
}
```

### 포스트 전부다 가져오기

- GET /api/posts/

### 해당 id값의 포스트 가져오기

- GET /api/posts/:id

### 해당 페이지의 포스트 가져오기

- GET /api/posts?username=&tag=&page=

> page마다 최대 포스트 : 10  
> 'Last-page' 정보는 Request Headers에 있음.  
> username과 tag로 해당 페이지 찾아올수있음.

### 해당 id값의 포스트 삭제하기

- DELETE /api/posts/:id

### 해당 id값의 포스트 수정하기

- PATCH /api/posts/:id

```json
/* Request body */
{
  "title": "수정",
  "body": "수정 내용",
  "tags": ["수정태그1", "수정태그2"]
}
```

---

## user API

### 회원가입

- POST /api/auth/register

```json
/* Request body */
{
  "username": "username",
  "password": "password"
}
```

### 로그인

- POST /api/auth/login

```json
/* Request body */
{
  "username": "username",
  "password": "password"
}
```

### 로그인 상태 확인하기

- GET /api/auth/check

### 로그아웃

- POST /api/auth/logout

## Environments

- koa@2.13.1
- koa-router@10.0.0
- koa-static@5.0.0
- koa-bodyparser@4.3.0
- bcrypt@5.0.1
- dotenv@8.2.0
- esm@3.2.25
- joi@17.4.0
- jsonwebtoken@8.5.1
- mongoose@5.11.19
- sanitize-html@2.3.3
