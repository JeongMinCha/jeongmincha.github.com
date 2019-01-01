---
layout: page
title: Projects (KO)
permalink: /projects/ko/
---

<hr/>
<center>요약</center>
<hr/>
- 회사에서 했던 프로젝트 업무들은 시각 자료 및 코드 첨부가 어려워 이곳에서는 작성하지 않고, 경력서 (Resume) 에 간단 서술해두었습니다.
- 5개의 연구 프로젝트
  - 4개는 대학원에서, 1개는 대학교 연구실에서 진행하였습니다. 모든 연구 프로젝트는 팀 프로젝트였습니다.
- 5개의 개발 프로젝트
  - 2개의 개인 프로젝트 (이 중 1개는 외주 프로젝트), 3개의 팀 프로젝트를 진행하였습니다.

<hr/>
<center>1. 연구 프로젝트 포트폴리오</center>
<hr/>
1) **Elicast: Embedding Interactive Exercises in Instructional Programming Screencasts** (L@S 2018) (2017.09 - 2017.12)
  - 상호작용이 가능한 스크린캐스트 형식의 프로그래밍 강의 플랫폼을 제시하고, 이 플랫폼의 효용성을 검증 
  - <iframe width="560" height="315" src="https://www.youtube.com/embed/dKWlqDLgsm8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  - [Paper](http://uilab.kaist.ac.kr/public/research/LAS2018/las2018_park.pdf)
  - [Slides](http://uilab.kaist.ac.kr/public/research/LAS2018/las2018_park_slides.pdf)
  - [ACM DL](https://dl.acm.org/citation.cfm?id=3231657)
<p />

2) [**An Imputation Method Using Directly Connected Neighbors in a Trust Network for Recommendation**](research/2015/01/01/recomendation-system/) (2015.01 ~ 2015.10)
  - 신뢰 네트워크에서 직접 연결된 이웃만을 활용하여 평점 행렬을 채우는 방법을 제시하고, 본 방법의 효용성을 검증  
  - <img src="/assets/projects/research/recommender-system/capture1.png" width="320" />
  - <img src="/assets/projects/research/recommender-system/result1.png" width="320" /> | <img src="/assets/projects/research/recommender-system/result2.png" width="320" /> | <img src="/assets/projects/research/recommender-system/result3.png" width="320" /> |
  - [Codes at GitHub](https://github.com/jeongmincha/Trust-based-Imputation)
  - [Paper](/assets/projects/research/recommender-system/recommender-system-paper.pdf) (3 pages)
  - [Report](/assets/projects/research/recommender-system/recommender-system-report.pdf) (21 pages)
<p />

3) [**Best Phrases for Successful Crowdfunding Projects**](research/2017/03/01/crowdfunding/) (2017.03 - 2017.06)
  - 크라우드 펀딩 프로젝트의 설명 글에서 쓰기에 효과적인 구와 절을 NLP 기법으로 파악  
  - ![](/assets/projects/research/crowdfunding/capture.png)
  - [Codes at GitHub](https://github.com/jeongmincha/best_phrases_for_successful_crowdfunding)
<p />

4) [**Phased LSTM with modified time gate function**](research/2017/03/01/phased-lstm/) (2017.03 - 2017.06)
  - Phased LSTM 모델에서 time gate 함수 식을 변경해서 성능 향상을 도모  
  - <img src="/assets/projects/research/phased_lstm/result-1.png" width="480" />
  - [Codes at GitHub](https://github.com/jeongmincha/Advanced-Phased-LSTM/tree/master/VariablePhasedLSTM)
<p />

5) **Word Embeddings for English Subtitles to catch familiarity between actors** (2017.08 - 2018.08)
  - 영어 자막 스크립트 데이터에서 등장하는 entity를 찾고, entity 간 친밀도를 계산  
  - <img src="/assets/projects/research/vtt/result.png" width="560" />
  - [Codes at GitHub](https://github.com/jeongmincha/word_embedding_for_subtitles)
<p />

※ Kaggle 프로젝트 했었던 코드들
 - <https://github.com/jeongmincha/gettingstarted-kaggle/tree/master/NewYorkTaxiTripDuration>
 - <https://github.com/jeongmincha/gettingstarted-kaggle/tree/master/titanic>
 - <https://github.com/jeongmincha/The_Nature_Conservancy_Fisheries_Monitoring>
 - <https://github.com/jeongmincha/SantanderCustomerSatisfication>

<hr/>
<center>2. 개발 프로젝트 포트폴리오</center>
<hr/>
1) [**키다리 은행 클라이언트 및 서버 개발**](development/2016/06/01/kidaribank/) (2016.05 ~ 2016.12)
  - 대학생에게 필요한 돈을 모금하고, 출자도 할 수 있는 키다리 은행 플랫폼 서비스를 풀 스택 개발  
  - <img src="/assets/projects/development/kidari/capture1.png" width="240" />  |  <img src="/assets/projects/development/kidari/capture2.png" width="240"/> | <img src="/assets/projects/development/kidari/capture3.png" width="240"/>
  - API Server: Python Flask, PostgreSQL
  - Front-end (App): Ionic 2 (Typescript)
  - [Flask API Server Codes at GitHub](https://github.com/jeongmincha/KidariBankFlaskAPIServer)
  - [Push Polling Server Codes at GitHub](https://github.com/jeongmincha/KidariBankPushPollingServer)
  - [Front Ionic App Codes at GitHub](https://github.com/jeongmincha/KidariBankApplication)
<p />

2) [**Waterful (수분 섭취 보조 애플워치 응용 프로그램)**](development/2015/09/01/waterful/) (2015.09 ~ 2015.11)
  - 수분 섭취하기 좋은 시간을 파악해 알림을 보내는 애플워치 응용 프로그램  
  - <img src="/assets/projects/development/waterful/capture1.png" height="400"> | <img src="/assets/projects/development/waterful/capture2.png" height="400">
  - iOS Companian App + Apple Watch (Swift)
  - [Codes at GitHub](https://github.com/maestro06-waterful/waterful)
<p />

3) [**stemfriend**](development/2017/07/01/steemfriend/) (2017.07 ~ 2017.07)
  - 블록체인 소셜 플랫폼인 steemit에서 유저랑 가장 친한 친구를 찾아주는 서비스  
  - <img src="/assets/projects/development/steemfriend/img.jpeg" width="320" />
  - Python Django, SteemSQL
  - [Codes at GitHub](https://github.com/jeongmincha/steemfriend)
<p />

4) [**안드로이드 폰과 블루투스 전동차를 활용한 방범 시스템**](development/2014/09/01/android-system/) (2014.09 ~ 2014.12)
  - 모션 인식으로 CCTV 역할을 하는 안드로이드 폰과 전동차를 제어하고 주인의 얼굴을 인식하는 안드로이드 폰을 이용한 방범 시스템  
  - <img src="/assets/projects/development/android_robot/capture.png" width="560" />
  - Android, TCP Server, Bluetooth Robot Control, Face & Motion Recognition
  - [Codes at GitHub](https://github.com/jeongmincha/cctv_using_android)
<p />

5) [**OpenWrt 공유기를 활용한 통합 파일 공유 시스템**](/projects/ko/development/2014/03/01/openwrt/) (2014.03 ~ 2014.06)
  - 공유기에 인터넷을 리스하고 있는 스마트폰, 노트북의 파일 시스템을 외부 인터넷에서 접근, 관리할 수 있게 하는 시스템  
  - <img src="/assets/projects/development/nad/capture.png" width="560" />
  - PHP, MySQL, Embedded Linux
  - [Codes at GitHub](https://github.com/jeongmincha/nad)
<p />

