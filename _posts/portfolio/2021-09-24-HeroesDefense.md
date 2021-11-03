---
layout: post
title: 히어로즈 디펜스 \: 좀비어택
author: twozeronine
categories:
  - portfolio
tags: [CSharp, Unity]
date: 2021-06-14 12:00 +0800
last_modified_at: 2021-09-24 01:08:25 +0800
---

<center>
<span style=
"font-size:170%;
font-weight:bold">
히어로즈 디펜스 : 좀비 어택
</span>
</center>

---

<center>사용 언어 : C#</center>
<center>개발 환경 : Unity3D</center>
<center>게임 장르 : 수집형 Defense</center>
<center>목표 플랫폼 : 모바일</center>
<center>타깃 국가 : 글로벌</center>
<center>개발팀 : ㈜ Dodam Games</center>
<center>당담역할 : 컨텐츠 개발 및 시스템 개발</center>
<br/>

[※ 구글 플레이 바로가기](https://play.google.com/store/apps/details?id=com.dodamgames.aos.newdefense)

<iframe width="788" height="488" src="https://www.youtube.com/embed/0Ct5K-o4hcI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

## 개요

제가 실무에서 프로그래밍을 하며 작업한 첫 번째 프로젝트입니다.

게임 장르는 수집형 디펜스로써, 수집 형식으로 히어로를 모아 전략적으로 기지를 방어하는 게임입니다.  
모바일 플랫폼으로 개발하였습니다.

프로젝트 진행시 저는 컨텐츠 개발 및 시스템 개발 역할을 맡았으며 주로 UGUI를 사용하여 상점, 컨텐츠 알림, 룬 장비 등 UI / UX View 로직을 당담하였고, Unirx와 UniTask를 사용하여 MVP 패턴으로 코드를 분리하고 Unity Addressable을 적용하여 비동기적으로 동작하는 프로그래밍을 하였습니다.

부로는 월드맵, 게임 스테이지를 Json으로 parsing 하여 미니맵 제작, git-flow 적용, Docker를 사용하여 Redmine 환경 구성, 개선사항 대응, 버그 수정등을 당담 하였습니다.

## Tech Stack

- Unirx를 사용하여 MVP 패턴으로 코드를 분리하여 로직과 View를 분리해 유지보수 하기 쉬운 코드 구현
- Unity Addressable를 적용하고 UniTask를 사용하여 비동기적으로 동작하는 프로그래밍 구현
- 룬 관련 컨텐츠 시스템 부터 모두 구현
