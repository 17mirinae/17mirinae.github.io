---
layout: post
title: AWS Certified Cloud Practitioner 101-150
date: 2021-04-08 22:29:00
categories: AWS
tags: AWS
---

(Q101) AWS Snowball 은 클라우드 안팎으로 페타 바이트의 데이터를 전송하도록 설계된 AWS 스토리지 서비스이며 두 가지 옵션으로 제공되는 엣지 컴퓨팅, 데이터 마이그레이션 및 엣지 스토리지 디바이스이다.

(Q101) Snowball 은 특정 Amazon EC2 인스턴스 유형과 AWS Lambda 함수를 지원하므로 AWS 클라우드에서 개발과 테스트를 마친 다음 원격 위치의 디바이스에 어플리케이션을 배포하여 데이터를 수집, 사전 처리하고 AWS 에 보낼 수 있다.

(Q102) 신뢰성 - 인프라 또는 서비스 중단으로부터 복구하고 수요를 충족하기 위해 컴퓨팅 리소스를 동적으로 확보하는 시스템의 기능

(Q103) AWS Elastic Beanstalk 은 어플리케이션의 응답성을 모니터링하는 것을 지원하기 위해 어플리케이션에 대한 통계를 모니터링하고 임계값을 초과하면 트리거되는 알림을 생성할 수 있는 기능을 제공한다.

(Q104) AWS Concierge is a senior customer service agent who is assigned to your account when you subscribe to an Enterprise of qualified Reseller Support plan. AWS Concierge agent is your primary point of contact for billing or account inquiries. [AWS 결제 및 AWS Support 를 위한 기본 연락처]

(Q105) AWS 클라우드는 고객의 실행 속도와 민첩성을 높이기 위해서 무엇을 제공합니까? <b style="color: red;">문의 필요</b>

(Q106) AWS Well-Architected Framework 에 따르면 AWS 클라우드의 안정성을 달성하기 위해 어떤 변경 관리 단계를 수행해야 합니까? <b style="color: red;">문의 필요</b>

(Q107) AWS 클라우드의 장점
- 민첩성 [광범위한 기술에 쉽게 액세스할 수 있으므로, 필요에 따라 리소스를 빠르게 구동할 수 있다]
- 탄력성 [필요한 만큼 리소스를 프로비저닝하면 된다]
- 비용 절감 [자본 비용 (데이터 센터, 물리적 서버) 을 가변 비용으로 전환하고 사용한 만큼만 IT 비용을 지불한다]
- 몇 분 만에 전 세계에 배포 [전 세계에 인프라가 있으므로 사용자는 클릭 몇 번으로 여러 물리적 위치에 어플리케이션을 배포할 수 있다]
<b style="color: red;">이 빌어먹을 선택지들은 왜 AWS 홈페이지에 장점이라 설명되어 있지 않은가...</b>

(Q108) AWS 책임 분담 모델에 따라 고객이 관리하는 것
Amazon EC2 인스턴스를 배포하는 고객은 게스트 운영 체제의 관리 (업데이트, 보안 패치 등), 고객이 인스턴스에 설치한 모든 어플리케이션 소프트웨어 또는 유틸리티의 관리, 인스턴스별로 AWS 에서 제공한 방화벽 (보안 그룹이라고 부름) 의 구성 관리에 대한 책임이 있다.

Amazon S3 및 Amazon DynamoDB 와 같은 추상화 서비스의 경우, 고객은 데이터 관리 (암호화 옵션 포함), 자산 분류, 적절한 허가를 부여하는 IAM 도구 사용에 책임이 있다.

(Q109) AWS 공동 책임 모델에서 AWS Lambda 기능을 관리할 때 고객이 책임지는 것
<img src="/assets/image/2021-04-08-AWS Certified Cloud Practitioner 101-150/1.png" width="100%" height="100%" />

(Q110) 회사의 IT 리소스 관리 책임을 덜어주기 위해 수행하는 IT 작업
데이터베이스 백업, 운영 체제 설치

(Q111) 