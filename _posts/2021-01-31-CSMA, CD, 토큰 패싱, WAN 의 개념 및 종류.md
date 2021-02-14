---
layout: post
title: "네트워크 관리사 - CSMA/CD, 토큰패싱, WAN 의 개념 및 종류"
date: 2021-01-31 18:35:00
categories: Network
tags: Certification Network
---

<h4>네트워크 일반 : CSMA/CD, 토큰 패싱, WAN 의 개념 및 종류</h4>

<h5>LAN 의 매체 접근 방법에 따른 분류</h5>

- 매체 접속 제어 방식에는 집중 제어 방식과 분산 제어 방식이 있으며, 집중 제어 방식으로 라운드 로빈 (Round Robin) 방식 대표적임

- LAN 에서는 일반적으로 분산 제어 방식이 사용되는데 이 방식은 경쟁 (Contention) 방식과 토큰 제어 방식으로 구분됨

- <p style="color: red;">경쟁 방식</p>에서는 각 지국이 필요시 아무 때나 매체에 접근할 수 있으며, <p style="color: red;">토큰 제어 방식</p>에서는 전송 권한을 부여하는 토큰을 사용하여 정해진 순서나 시간에 따라 매체에 접근하게 됨

- 경쟁 방식의 대표적인 예로는 ALOHA, CSMA/CD 방식이 있고, 토큰 제어 방식으로는 토큰 버스, 토큰 링 방식이 있음

1. CSMA / CD (Carrier Sense Multiple Access / Collision Detection)
    - 데이터 전송 전 통신 회선의 사용 여부를 파악하기 위해 Carrier Sense 를 보내 반송파 여부를 감지함
    - 사용 중이면 송신하지 않고, 사용하고 있지 않으면 송신함
    - 버스형, 성형으로 LAN 에 많이 사용됨

    <img src="/assets/image/2021-01-31-CSMA, CD, 토큰 패싱, WAN 의 개념 및 종류/1.png" width="100%" height="100%" />
    
    - Multiple Access 방식에서는 채널이 비어있는 것으로 판단되면 각 노드 중 누구라도 데이터를 전송할 수 있음

    <img src="/assets/image/2021-01-31-CSMA, CD, 토큰 패싱, WAN 의 개념 및 종류/2.png" width="100%" height="100%" />
    
    - Collision Detection 방식에서는 충돌 발생 시 데이터 프레임 송신을 중단함

    <img src="/assets/image/2021-01-31-CSMA, CD, 토큰 패싱, WAN 의 개념 및 종류/3.png" width="100%" height="100%" />

2. 토큰 패싱 (Token Passing) 방식
    - 대표적인 것은 토큰 링 방식
    - 토큰이라는 신호를 전송
    - 부하가 증가하게 되면, 그 증가에 대한 영향은 적은 반면에, 낮은 부하에도 오버헤드가 발생할 수 있음
    - 통선 회선의 길이가 제한이 없음
    - 노드의 수가 많으면 충돌 가능성 높아짐
    - 전송 매체는 토큰 링에서 평형 케이블, 토큰 버스에서 동축 케이블 사용

    <img src="/assets/image/2021-01-31-CSMA, CD, 토큰 패싱, WAN 의 개념 및 종류/4.png" width="100%" height="100%" />
<br><br>
<h5>WAN 의 개념과 구성요소</h5>

<b style="color: red;">WAN (Wide Area Network) 의 개념</b>
- WAN 이란 멀리 떨어진 LAN 이나 내선 전화망을 상호 연결하기 위한 다리 역할을 하는 광범위 대규모 네트워크
- 보통 KT, SK, LG 같은 전기 통신업자가 운영하고, 우리는 서비스 요금을 지불하고 WAN 회선을 사용함
- WAN 에서는 데이터를 Point To Point 방식으로 주고 받음

<img src="/assets/image/2021-01-31-CSMA, CD, 토큰 패싱, WAN 의 개념 및 종류/5.png" width="100%" height="100%" />

- 대표적인 WAN 으로는 인터넷이 존재함

<b>WAN 의 특징</b>
- 지역성이 제한이 없음
- 원거리 통신은 대체 느림
- 여러 LAN 과 상호 작용
- LAN 보다 복잡하고 어려움
- 기술적인 비용이 비쌈
- LAN 구간의 연결이라도 매체 특성상 원거리일 경우에는 WAN 을 이용해 연결함

<b style="color: red;">WAN 의 종류</b>
- ISDN (Integrated Service Digital Network : 종합정보통신망) 은 각종 통신서비스마다 개별적으로 운영되고 있는 기존통신망과는 달리 음성, 데이터, 영상 등 다양한 형태의 정보를 하나의 통합된 망에서 제공하는 고속, 고품질의 경제적인 디지털 통신망
- PSTN (Public Switched Telephone Network : 공중전화교환망)
    - 과거로부터 사용되던 일반 공중용 아날로그 전화망을 지칭
    - 통상적으로 데이터 망과는 별도로, 재래의 전화위주의 유선 통신망이라는 의미가 강함
    - 이에 사용되는 기본 기술로는 회선 교환이며, 패킷 교환망과는 차별됨
    - 일반 사용자들 대상으로 모뎀을 이용해서 여러 데이터 통신도 가능하게 하고 있음
- 프레임 릴레이
    - 장거리 통신망 (WAN) 에서 사용하는 링크 레이어 프로토콜 중의 하나
    - 하나의 포트를 통하여 여러 개의 네트워크 포트와 연결할 수 있음
- ATM (Asynchronous Transfer Mode : 비동기 전달모드) 는 회선교환의 실시간성 및 패킷 교환의 유연성을 통합시킨 연결지향적 패킷 교환 복합 기술
    - 주소 포맷, 신호 방식 등 회선 교환 방식을 이용
    - ATM 셀 처리 등은 패킷 교환 방식 이용
- SMDS (Switched Multi-megabit Data Service)
- SONET (Synchronous Optical NETwork)
    - 음성, 영상 등 다양한 종류의 서비스를 전송
    - 광섬유 전송 시스템 장비의 표준화를 위해 사용