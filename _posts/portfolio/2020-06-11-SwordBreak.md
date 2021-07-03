---
layout: post
title: 검이 터졌다
author: twozeronine
categories:
  - portfolio
tags: [CSharp, Unity]
date: 2020-06-11 18:18 +0800
last_modified_at: 2020-08-17 01:08:25 +0800
---

<center>
<span style=
"font-size:170%;
font-weight:bold">
팀 뉴메타의 검이 터졌다
</span>
</center>

---

<center>사용 언어 : C#</center>
<center>개발 환경 : Unity3D</center>
<center>목표 플랫폼 : 모바일</center>
<center>개발팀 : Team_Newmeta</center>
<center>당담역할 : 메인프로그래밍</center>
<br/>

[※ 텀블벅 바로가기](https://www.tumblbug.com/cc4811eb-823c-4315-aa76-3348fed1e1b2)

<a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/tTWjvVm8/image.gif" alt="image"/></a><br/><br/>

> 메인 오프닝 화면

---

<a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/c17WQw3n/2.gif" alt="2"/></a><br/><br/>

> 메인 오프닝 화면 2

---

<a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/FzvQMsMz/image.gif" alt="image"/></a><br/><br/>

> 게임 시작시 시놉시스

---

![시네마틱](https://tumblbug-psi.imgix.net/250e1883946f7e5d003469bb923dbd8a48af7250/6eec8030c730675bec7c1ff93f61a08162934ebd/b48418b111890927aeb920ef3b8d2d6504da215b/05285d36-a020-4e90-9790-b90e8391c92e.gif?ixlib=rb-1.1.0&w=1240&auto=format%2C%20compress&lossless=true&ch=save-data&gif-q=35&s=c2975914eea01d2156d4f2ec1d4f3a21)

> 게임 진행 중 검이 터지는 시네마틱

---

![전투피격상황](https://tumblbug-psi.imgix.net/250e1883946f7e5d003469bb923dbd8a48af7250/6eec8030c730675bec7c1ff93f61a08162934ebd/b48418b111890927aeb920ef3b8d2d6504da215b/9f646c6b-2f95-4942-89d3-20c57aa965f7.gif?ixlib=rb-1.1.0&w=1240&auto=format%2C%20compress&lossless=true&ch=save-data&gif-q=35&s=37737f33e21abc7f1f4eba35ed6afe14)

> 전투 피격 상황

---

![광란 일반공격](https://tumblbug-psi.imgix.net/250e1883946f7e5d003469bb923dbd8a48af7250/6eec8030c730675bec7c1ff93f61a08162934ebd/b48418b111890927aeb920ef3b8d2d6504da215b/4aa417a5-3b60-425d-b0e4-2d16c5fbcb7a.gif?ixlib=rb-1.1.0&w=1240&auto=format%2C%20compress&lossless=true&ch=save-data&gif-q=35&s=ba8dcc9f0d169ea6dea788325a0265b6)

> 광란 일반공격

---

![광란 스킬공격](https://tumblbug-psi.imgix.net/250e1883946f7e5d003469bb923dbd8a48af7250/6eec8030c730675bec7c1ff93f61a08162934ebd/b48418b111890927aeb920ef3b8d2d6504da215b/5da3ddd2-03a9-44df-bf26-a1339abefdd8.gif?ixlib=rb-1.1.0&w=1240&auto=format%2C%20compress&lossless=true&ch=save-data&gif-q=35&s=9077bc511880b5ed964a5b5e06f5efe5)

> 광란 스킬공격

---

![오래된 옛 친구 스킬공격](https://tumblbug-psi.imgix.net/250e1883946f7e5d003469bb923dbd8a48af7250/6eec8030c730675bec7c1ff93f61a08162934ebd/b48418b111890927aeb920ef3b8d2d6504da215b/b8053053-c054-4bec-a251-f44c2faec7d7.gif?ixlib=rb-1.1.0&w=1240&auto=format%2C%20compress&lossless=true&ch=save-data&gif-q=35&s=7f5a03c6777352bda58990e5db85d6fc)

> 오래된 옛 친구 스킬공격

---

![image](https://user-images.githubusercontent.com/67315288/124350293-d1b77680-dc2e-11eb-8b86-c96efccd1b0d.png)

> 미니맵

---

## 개요

제가 게임 프로그래밍을 하며 팀으로 작업한 첫 번째 프로젝트입니다.

게임 장르는 로그 라이트로써, 빠른 전투를 필요로 하는 핵앤슬래쉬 스타일 게임입니다.  
모바일 플랫폼과 PC로 개발하였습니다.

프로젝트 진행시 저는 메인 프로그래밍 역할을 맡았으며 주로 팀원들이 프로그래밍 하거나 디자인하며 만든 것들을 하나의 클라이언트에 모아 제작하는 역할을 하였습니다.

부로는 게임 스테이지, 랜덤 맵, 미니맵, 몬스터 AI, 유저나 몬스터 데이터 베이스, 시네마틱, UI를 구현하였으며 디버깅 하며 버그를 수정해 나가는 역할을 하여 전체적인 클라이언트를 당담하였습니다.

## Tech Stack

- 기획자가 텍스트 파일로 구현한 맵을 유니티상에서 불러와 구현
- 게임 진행을 위한 스테이지 구현
- CineMachine과 Timeline 사용으로 인게임 시네마틱 영상을 만듬
- NavMesh를 사용하여 몬스터 AI 구현
- ScriptableObject를 사용하여 유저와 몬스터 데이터 베이스를 저장함
- 게임 진행에 필요한 전투, 미니맵의 UI/UX를 구현함
- SoundManager를 구현하여 게임내에서 배경음악과 효과음등을 사용함
