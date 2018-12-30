---
layout: post
title: Phased LSTM with modified time gate function 
categories: [projects, ko, research]
tag: []
---

- 참여기간
  - 2017.03 - 2017.06
- 프로젝트 개요
  - 베이스라인인 PhasedLSTM 에서 사용하는 time gate 함수를 변조해보면서 N-MNIST데이터셋 (**MNIST셋과 다름**)을 쓰는 기존 실험에서 더 큰 성능을 보이는 모델을 찾아봄.
  - PhasedLSTM은 LSTM 모델에서 cell 앞에 시간 (t) 에 종속적인 time gate 함수를 추가하여 긴 시퀀스의 데이터를 더 효율적으로 처리하는 모델인데, 주로 다양한 센서가 비동기적으로 데이터를 주입하는 긴 시계열 데이터를 처리하는 데 쓰인다.
  - time gate 함수의 open phase (cell을 업데이트하는 순간) 를 선형에서 이차 함수로 변경해보고 (**qPLSTM**), 해당 함수의 close phase (cell을 업데이트하지 않는 순간) 를 leaky function에서 constant function으로 변조하였다. (**clPLSTM**)
  - 그 결과 최종적으로 수렴 정확도는 기존과 큰 변화 없었으나, 더 빠른 수렴을 보여주었다.

<img src="/assets/projects/research/phased_lstm/result-1.png" />

<hr/>
<center>주요 역할 및 담당</center>
<hr/>
- 총 3명이 담당하였고,
- 본인이 실험을 위한 코드 작성 및 실험을 주도하였고,
- 나머지 인원은 수식 아이디어 제시, N-MNIST 데이터 정제, 및 베이스라인 모델인 Phased LSTM 코드를 구해주는 등 부가적인 일을 보조해주었다.

<hr/>
<center>성과</center>
<hr/>
- N-MNIST 데이터 셋을 처음 접함
- 기존 논문 모델의 코드를 뜯어보면서 핵심 코드 부분을 수정해서 추가 실험을 해보는 경험을 가짐