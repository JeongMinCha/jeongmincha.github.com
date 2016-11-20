---
layout: post
title: 키다리 은행 외주 개발에서 사용한 기술들
---

첫 풀스택 외주 개발인 [키다리 은행]을 개발하면서 배운 것들이 많은데, 그들을 남기고 복습하기 위해서 포스트를 작성하게 됨.

### 플랫폼
- API 서버: Flask
- 클라이언트: Ionic2 Framework
    - iOS와 Android를 동시에 개발하기 위해서 Ionic2 Framework를 사용함.

### 로그인
- BasicAuth
- Password Encryption by SHA256

### 푸쉬 서버
- FCM Server
- APNS Server