---
layout: post
title: 블록체인 소셜 플랫폼 steemit 친구를 찾아주는 stemfriend
categories: [projects, ko, development]
tag: [development, projects, blockchain, python, django, korean]
---

![](/assets/projects/development/steemfriend/img.jpeg)
- 참여기간
  - 2017.07 - 2017.07
- 프로젝트 개요 
  - 블록체인 소셜 플랫폼 중 하나인 steemit에서 가장 친한 친구를 찾아주는 웹 서비스를 만듬. 페이스북에서 가장 친한 친구를 찾아주는 서비스를 보고 아이디어를 생각하게 됨.

<hr/>
<center>주요 역할 및 담당</center>
<hr/>
- 혼자서 진행한 프로젝트로, Django 프레임워크를 이용하여 블록체인 데이터를 가져와 분석하고, 웹사이트에 뿌려주는 역할을 함.

<hr/>
<center>발생 문제 및 해결 방법</center>
<hr/>
- 처음에 단순 구현 후에는 Bad Gateway 가 자주 발생. 한 유저가 들어간 후 몇 초간의 계산 후에 결과가 나오게 되는데, 동시 접속이 많은 경우 이러한 문제가 발생했음.
  - ☞ Nginx 및 Django 설정을 통해 다중 접속시에도 서버 접속이 원활해지도록 해결함.

- 사용자의 인터랙션 히스토리를 가져와야 하는데, steemit 블록체인에서 제공하는 API를 굉장히 많이 호출해야 했고, 그로 인해 한 사람당 30초 가까이 기다려야 하는 문제가 발생하였음.
  - ☞ steemit 블록체인 데이터를 SQL처럼 처리할 수 있는 SteemSQL을 사용하여 데이터 베이스 내에서 최대한 효율적인 처리를 한 후에 결과를 가져올 수 있도록 구현하여 해결함.

<hr/>
<center>성과</center>
<hr/>
- 블록체인에 올라가 있는 소셜 데이터에 접근해볼 경험을 가짐.
- Django 프레임워크로 개인 토이 프로젝트를 처음 해봄.
- 웹 서버 엔진 Nginx, uwsgi를 직접 세팅.
- 속도 개선을 위한 고민을 해본 경험.

<hr/>
<center>개발 당시 블로그 글</center>
<hr/>
- <https://steemit.com/kr/@jeongmincha/steemfriend>
- <https://steemit.com/kr/@jeongmincha/steemfriend-1>
- <https://steemit.com/kr/@jeongmincha/steemfriend-2>
- <https://steemit.com/kr/@jeongmincha/steemfriend-3>
