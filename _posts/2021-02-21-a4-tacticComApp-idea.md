---
title:  "화이트 보드"
excerpt: "내 방 화이트보드에 있는 것을 지우기위한 글"

categories:
  - a4
tags:
  - idea
last_modified_at: 2021-02-21
---

# tactical communication mobile application(aka. TaCoMo)
* 영감
    - 육군 무전기
    - 카카오톡 단체톡방

* 해결하려고 하는 점
    - 친구끼리 놀러 모일때 한명한명 연락하면서 위치 찾기에 어려움이 있다
    - 처음 가는 곳은 길을 잃기 쉽다
    - 서로 어디있는지를 모른다
    - 그냥 모일때 연락해서 위치 유도하기가 귀찮다

* 어떻게 해결?
    - 원하는 모임끼리 방을 만든다
    - 지도 api 이용
    - GPS 로 서로 위치 공유(모임끼리)
    - 전체통화 기능 또는 pushToTalk 버튼 기능으로 서로 음성 회의
    - 지도에 펜으로 그림을 그릴 수 있어야함(이것이 바로 공유)

* 예상되는 시스템의 문제점 & 해결책
    - 서버가 해킹당했을시 도청이 가능 :: 해당 톡방의 인원이 공개키 방식으로 대칭키를 교환 -> 대칭키로 서로 통신 
    - GPS를 공유하고싶지않은 모임이 있을 수 있음 :: 각 방마다 수준을 정해서 private 또는 public 으로 스위칭 가능하게 -> default 는 private(GPS미공유)

* 구조
    - 모바일 어플리케이션 name TaCoMo
    - 음성교환, 채팅 서비스 서버
    
* 필요한 기술
    - 방 초대 -> fcm
    - 채팅 -> 롱폴링(active), FCM(to wakeup), ActiveMQ
    - 지도 api 
    - 지도 api 에 그림 넣는 기술 (2d 라이브러리?)
    - 다대다 실시간 음성 통화 
    - 회원가입 & 로그인 -> oauth2.0 인증 -> 카카오, 구글, 네이버, 등등 (이메일이 존재하는 사이트 계정 페이스북은 XXX)

* 세부 요구사항
    - 채팅 저장 시간 -> 3일 (3일 지난 것은 매일 새벽 12시에 일괄 제거)
    - 인증 jwt토큰
    - 채팅용 데이터베이스는 MongoDB
    - 기타 -> mysql
    - https://changicho.tistory.com/entry/WebRTC-00-%EA%B8%B0%EC%B4%88
    - http://www.gilgil.net/?mid=communities_kr&comment_srl=7102&listStyle=webzine&page=11&document_srl=18378
    - https://rlg1133.tistory.com/90
    - https://www.html5rocks.com/ko/tutorials/webrtc/infrastructure/
    - STUN(홀펀칭), TURN 방식


