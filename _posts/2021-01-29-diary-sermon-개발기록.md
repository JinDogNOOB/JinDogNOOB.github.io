---
title:  "고민 공유 sermon 개발기록"
excerpt: ""

categories:
  - diary
tags:
  - react
  - spring-boot
  - hibernate
  - material-ui
last_modified_at: 2021-01-29
---

```
포트폴리오용 프로젝트가 없길래 급하게 10일정도를 투자해서 만든 
sermon, sermon-front, 가 끝났다.
url: https://github.com/JinDogNOOB/sermon
url: https://github.com/JinDogNOOB/sermon-front

sermon에는 spring boot, restapi, orm jpa hibernate, paging, #검색, spring security, TDD 등의 기술을 사용했다.
하면서 조금 도움이 됬던 것은 spring security를 실제로 적용해봄으로써 filter와 interceptor 에 조금 적응했던것이다
그리고 TDD 기반 개발을 하면서 service layer정도만 테스트 케이스를 작성해서 진행했는데, 개발 오류 발견에 정말 큰 도움이 됬던 것 같다.
특히 페이징 관련해서 테스트할때 도움이 많이 됬던것같다. 
1년전의 나였으면 전부 개발하고 html을 짜거나 PostMan을 사용해서 일일히 테스트했다. 
정말 힘들뻔했는데, 이래서 TDD TDD 하는건가 보다.
service layer뿐만 아니라 controller에 대해서도 테스트 코드를 짤 수 있었지만 spring security 도 적용되어있기도해서 해야되는게 추가적으로 있었다.
그래서 service만 테스트 체크를 했고 나머지는 react 개발에 힘을 쏟았다.

sermon-front에는 react, hooks, context-api, redux 를 사용했는데 역시 가장 어려운 것은 ui-ux 이고 디자인이더라,,
상황이 상황이니만큼 트위터 메인페이지, 쓰레드 페이지를 조금 참고해왔는데,, 참고를 해도 css를 보고 이해를 해야했기때문에
본의아니게 css공부까지 했다. 진짜 꾸미는것은 어려웠다.
아 #검색 이거 구현한게 정말 나에게 정말 감동했다, 실제 sns마냥 추천 검색어가 밑에 absolute로 쫙 뜨고 그거 누르면 자동완성되고 한칸 띄어지고 
정말 그 희열이 느껴지더라, 예제코드 없이 내가 손수 짠 것이라서 더 그랬던 것 같다 ㅎㅎ,,,

아무튼 요즘 여기저기 일자리 넣어보고는 있는데 이 포폴을 추가함으로써 조금 더 힘이 될 것 같다.
```



