---
layout: post
title: 스팀잇에서 누가 나랑 가장 친할까? 👪 steemfriend 개발일지 #2
---

![](https://steemitimages.com/0x0/https://steemitimages.com/0x0/https://steemitimages.com/DQmXYoCFPhnX2etF7xu25i3gZw6ipocDrYuBoy4nBDqgseA/unnamed.jpg)

우선 오늘은 어제 있었던 일들에 대해서는 어느 정도 해결이 된 듯 합니다.

1. 특정 사용자의 히스토리를 분석 `get_account_history()`  
1. 특정 사용자가 쓴 글들을 다 취합하고 `repeat get_account_history()`  
1. 그 글들에 대해서 있었던 보팅 + 코멘트 히스토리를 취합 `get_content(), get_content_replies()`  
1. 어떠한 사람들이 나에게 가장 많은 보팅 + 코멘트를 해주었을까?  

를 통해 list-up을 해주는 것이 기본 아이디어의 흐름이었습니다. 우선 처음에는 간단하고 직관적으로 구현해놓고 그 뒤로 계속해서 피드백 받으면서 발전해 나가는 것이 중요하다고 생각했기 때문에 이 정도로 정리를 해봤죠.

어제 겪었던 문제는 특정 사용자가 쓴 글들을 다 취합한 후에 각 글마다의 보팅 + 코멘트 히스토리를 가져오는 데서 문제가 발생했었는데요. steemjs를 사용하는 대신 파이썬 코드로 웹소켓 URL에 직접 데이터를 취하면서 하니 금방되더군요. 이 작업이 어려운 일이 아니라 사소한 문제만 없었다면 하루 안에 충분히 해내야 할 일이었는데, JS가 확실히 데이터 핸들링하기에는 썩 좋은 언어가 아닌 것 같다고 느끼게 됬었네요... 😭

# 우선 나랑 가장 친한 사람은 누구??
보팅을 제일 많이 해주신 분  
| username | # of votes |  
| :------: | :--------: |  
|@tristan143|59|  
|@wooklym|56|  
|@vimva|37|  
|@smithkim|31|  
|@coinkorea|29|  
|@acceptkim|25|  
|@yoon|19|  
|@tmkor|19|  
|@leesunmoo|19|  
|@dimimp|18|  

댓글을 제일 많이 해주신 분  
| username | # of replies |  
| :------: | :----------: |  
|@greenjuice|15|  
|@acceptkim|15|  
|@vimva|15|  
|@subin0613|13|  
|@richbaek|13|  
|@steemitboard|13|  
|@woosungchoi|11|  
|@nand|9|  
|@nps0132|9|  
|@yoon|9|  

일단 제가 쓴 글에 대해서 보팅 + 댓글 히스토리를 살펴보니 위와 같더라구요. 각 10명씩 뽑아보았습니다. 정말 감사한 분들이 아닐 수 없습니다. 

# 이제 제가 그 다음으로 해야 할 일은 

1. steemfriend 홈페이지 안에서 댓글과 보팅에 대한 비중을 사용자가 선택할 수 있도록 할 것.  
1. 사용자가 선택한 비중을 통해서 steemfriend factor를 설정  
1. 위에서 설정한 factor를 기반으로 친한 사람들을 list-up해서 보여줄 것.  

입니다. 그리고 이 외에도 사실 아이디어가 정말 많습니다. 아시겠지만 첫 버전은 정말 단순하게 갈 것이기 때문에 복잡한 로직을 거의 다 제거하였습니다. 추가할 부분이라고 하면 날짜에 대한 부분 (누적 기록보다 최근에 얼마나 더 많은 교류가 있었는지) 이라던지, 보팅에 있어서는 보팅 파워 퍼센티지도 있고, 각 보팅을 통해 실제로 발생한 수익에 대한 부분. 교류가 있었던 사람의 여러 가지 정보들... 등 많은 부분을 고려하여 만들어 볼 수 있을 것입니다.

언제든지 여러분들의 생각을 들을 준비가 되어 있으니 이런 저런게 필요하겠다 싶으면 바로 말씀 부탁드리겠습니다 😉

# 그래도 맘 편하게 잘 수 있을 것 같네요
뭐 어쨌든 문제 없이 데이터 핸들링에 대한 첫 버전은 마무리가 되었고, 이제 이걸 클라이언트에서 이쁘게 잘 보여주도록 할 일만 남았네요. 이것도 최대한 단순한 디자인으로 깔끔하게 보여주는 형태로 금방 만들어보도록 하겠습니다. 첫 버전은 정말 딱 단순한 기능만 하는 형태로 만들어지겠죠? 다시 월요일이 다가오는 만큼 빠르게 마무리할 수 있을지는 모르겠습니다...ㅠㅠ 다들 힘내서 월요일을 맞아봅시다 👍

- 스팀잇에서 누가 나랑 가장 친할까? 👪 steemfriend 개발일지 #1  
  https://steemit.com/kr/@jeongmincha/steemfriend-1  
- 스팀잇에서 누가 나랑 가장 친할까? 👪 steemfriend 개발시작? 🚀  
  https://steemit.com/kr/@jeongmincha/steemfriend  


![](https://img1.steemit.com/480x0/https://steemitimages.com/DQmUdNLJKzrFrZNgsc1c5UkZWHkTwPZj8KXApQcs6deGDK5/follow%20image-min.png)
