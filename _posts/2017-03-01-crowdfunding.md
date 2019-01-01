---
layout: post
title: Best Phrases for Successful Crowdfunding Projects
categories: [projects, ko, research]
tag: []
---

- 참여기간
  - 2017.03 - 2017.06 
- 프로젝트 개요
  - 킥스타터 데이터를 활용하여 크라우드 펀딩에서 성공적인 모금을 하기 위해서는 어떠한 구, 절을 사용해야 하는지를 NLP 기법을 통해서 파악하는 프로젝트이다.
  - 크라우드 펀딩을 성공적으로 마무리했다는 것을 1) 모금한 돈의 액수 (pledged amount), 2) 모금자의 수 (the number of backers), 3) 모금을 달성한 퍼센티지 (percentage of funds) 로 정의하였다. 해당 크라우드 펀딩에서 쓰인 글을 n-gram 모델로 단어 벡터로 만들어서 feature로 사용했고, 이를 포함한 여러 feature들을 기반으로 앞서 정의한 성공의 지표들을 예측해내는 penalized linear regression 모델을 사용했다. 이 모델을 통해 성공의 지표를 높게 예측해내는 n-gram 단어 벡터를 찾아내었다.

![](/assets/projects/research/crowdfunding/capture.png)

<hr/>
<center>주요 역할 및 담당</center>
<hr/>
- 총 3명이 참여했고,
- 본인은 킥스타터 데이터 크롤링 / penalized linear regression 모델 구현 / 해당 모델을 평가 (evaluation) 하는 업무를 맡았다.
- 나머지 2명은 모델에 사용할 feature engineering, data cleaning, 크라우드 펀딩의 설명 글을 n-gram 데이터로 뽑아내는 업무를 맡았다.

<hr/>
<center>발생 문제 및 해결 방법</center>
<hr/>
- 매우 특별한 고유 명사가 결과값으로 도출되는 경우가 많았다. 아마도 특정 크라우드 펀딩이 크게 성공한 탓에 여러 크라우드 펀딩 글에서 자주 언급되었기 때문으로 사료된다. 
  - 더 큰 데이터를 사용하는 것으로 해결했다. 기존에는 약 4000개의 크라우드 펀딩 데이터를 활용하였으나, 50000개의 크라우드 펀딩 데이터를 활용하였다.
  - 전체 데이터셋에서 특정 횟수 이상은 쓰일 때만 n-gram에 포함시키도록 제한하였는데, 이 threshold값을 크게 높여 일반적으로 자주 쓰이는 명사만 결과로 나오도록 수정함. (사용하는 데이터셋이 커지면서 자연스럽게 그렇게 해야 했는데 결국 두 가지 요인 덕분에 문제를 해결하였다.)

<hr/>
<center>성과</center>
<hr/>
- NLP 기술에 사용할 데이터를 직접 크롤링
- 큰 크기의 텍스트 데이터 셋 전체를 정제하고, n-gram 모델을 사용해봄