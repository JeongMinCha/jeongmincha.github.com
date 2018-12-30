---
layout: post
title: 안드로이드 폰을 활용한 방범 시스템 개발
categories: [projects, ko, development]
tag: []
---

- 참여기간
  - 2014.09 ~ 2014.12
- 프로젝트 개요
  - 안드로이드 폰 두 개와 블루투스 제어 전동차인 BeautoRover로 방범 시스템을 개발하는 프로젝트.
  - 안드로이드 폰 하나는 CCTV역할을, 다른 하나는 BeautoRover를 제어하는 용도로 사용되었다. CCTV역할의 안드로이드 폰이 모션 인식과 얼굴 인식을 하였고, 시스템에 동록되지 않은 사용자일 경우 BeautoRover를 제어하는 안드로이드 폰과 통신하여 BeautoRover를 작동시켜서 방범 기능을 하는 방식이다.

<img src="/assets/projects/development/android_robot/capture.png" />

<hr/>
<center>주요 역할 및 담당</center>
<hr/>
- 총 2명이 참여한 프로젝트로, 다른 팀원은 모션 인식 기능 (Motion Recognition) 과 CCTV 역할을 하는 안드로이드 폰의 앱을 구현하였고,
- 본인은 인식된 사람이 시스템에 등록된 사람인지 아닌지를 구분하는 기능 (Face Recognition) 과 BeautoRover를 블루투스로 통신하고 제어하는 안드로이드 폰의 앱을 구현

<hr/>
<center>발생 문제 및 해결 방법</center>
<hr/>
- 2개 이상의 디바이스와의 블루투스 통신을 제어하는 것이 어려움
  - 안드로이드 폰과의 통신은 TCP 통신을 통하여 구현함.
- 얼굴 인식을 위해 OpenCV를 사용하려고 하였으나, 안드로이드 폰에서의 OpenCV가 예상보다 속도나 정확도가 좋지 못하였음.
  - 안드로이드 기본 hardware 패키지에서 제공하는 Camera.Face 클래스, FaceDetectionListener 등을 활용하여 구현하였음. 이들을 사용하여 인식된 얼굴의 정보를 알 수 있었고, 그 정보를 기반으로 얼굴을 식별하고 구별하는 기능을 구현하였음.
- 모션 인식이 너무 민감한 문제가 발생하였음
  - 아주 작은 모션 인식으로도 감지가 되는 문제가 발생하여, 수 차례 실험을 통해 pixel, image threshold를 제대로 설정하여 적절한 모션 인식을 유도함.

<hr/>
<center>성과</center>
<hr/>
- 안드로이드 플랫폼에서 블루투스 통신 기술, TCP 통신 기술, 얼굴, 모션 인식을 위한 기술 등 다양한 기술을 다뤄볼 수 있고, BeautoRover를 작동시키기 위한 레퍼런스 문서와 OpenCV를 대체할 다른 얼굴 인식 방법을 찾다가 안드로이드 hardware 패키지에 대한 레퍼런스 문서를 참고하였다.