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

(Q111) Amazon EC2 인스턴스를 중지한 특정 사용자를 식별하는데 사용할 수 있는 것
- 인스턴스가 AWS 를 통해 중지, 재부팅 또는 종료된 경우
    1. CloudTrail 콘솔을 연다.
    2. 탐색 창에서 이벤트 기록(Event History) 을 선택한다.
    3. 조회 속성(Lookup Attributes) 드롭다운 메뉴에서 이벤트 이름(Event Name) 을 선택한다.
    4. 인스턴스가 중지된 경우 이벤트 이름 입력(Enter An Event Name) 에 StopInstances 를 입력한다. 인스턴스가 재부팅된 경우 RebootInstances 를 입력한다. 인스턴스 종료된 경우 TerminateInstances 를 입력한다.
    5. 이벤트에 대한 자세한 내용을 보려면 이벤트 이름을 선택한다. StopInstances, RebootInstances 또는 TerminateInstances 이벤트 세부 정보 페이지에서 이벤트를 시작한 AWS Identity and Access Management(IAM) 사용자의 사용자 이름을 볼 수 있다.

- 인스턴스가 Windows OS 내에서 중지되거나 재부팅된 경우
    1. 이벤트 뷰어(Event Viewer) 를 연다.
    2. 탐색 창에서 Windows 로그(Windows Logs) 를 확장하고 시스템(System) 을 선택한다.
    3. 작업(Actions) 창에서 현재 로그 필터링(Filter Current Log) 을 선택한다.
    4. 모든 이벤트 ID(All Event IDs) 필드에 1074 또는 1076을 입력한다.
    5. 이벤트 로그의 소스(Source) 필드에 이벤트를 시작한 사용자가 표시된다.

(Q112) AWS 공동 책임 모델에서 고객의 책임은 어떤 보안 관행인가?
???
<b style="color: red;">문의 필요</b>

(Q113) 개체를 저장하고 해당 개체에 실시간으로 액세스하며 버전 관리 및 수명주기 기능을 제공하는 서비스
수명 주기 동안 객체가 비용 효율적으로 저장되도록 관리하려면 해당 Amazon S3 수명 주기를 구성한다.

(Q115) Elastic Load Balancing (ELB) 에서 사용할 수 있는 로드 밸런서 유형
ELB 에서 사용할 수 있는 로드 밸런서 유형으로는 4가지 유형이 있다.
- Application Load Balancer
- Network Load Balancer
- Gateway Load Balancer
- Classic Load Balancer

(Q116) Amazon EC2 용량을 구매할 수 있는 AWS 서비스
- 온 디맨드 인스턴스는 실행하는 인스턴스에 따라 시간당 또는 초당 컴퓨팅 파워에 대한 비용을 지불한다.
- 스팟 인스턴스는 온 디맨드 요금보다 최대 90% 할인된 가격으로 예비 Amazon EC2 컴퓨팅 용량을 요청할 수 있다.
- 예약 인스턴스는 온 디맨드 인스턴스 요금과 비교하여 상당한 할인 혜택을 제공한다.
- 전용 호스팅은 고객 전용의 물리적 EC2 서버이다. 온 디맨드 요금과 비교하여 최대 70% 할인된 예약 인스턴스로 구매 가능하다.

(Q117) S3 Glacier Deep Archieve 는 Amazon S3 중 가장 낮은 요금의 스토리지 클래스이며, 긴 기간동안 한두번 접근할 정도의 방대한 데이터를 보관하는 서비스를 제공한다.

(Q118) ???
<b style="color: red;">문의 필요</b>

(Q119) ??? NoSQL 사용하는 거 아니냐구...?
<b style="color: red;">문의 필요</b>

(Q120) 설명이 밑에 써져 있다.
AWS의 규정 준수 보고서에 온 디맨드 방식으로 액세스할 수 있도록 무료로 제공되는 셀프 서비스 포털은 AWS Artifact 이다.

AWS Artifact is your go-to, central resource for compliance-related information that matters to
you. It provides on-demand access to AWS' security and compliance reports and select
online agreements. Reports available in AWS Artifact include our Service Organization
Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from
accreditation bodies across geographies and compliance verticals that validate the
implementation and operating effectiveness of AWS security controls. Agreements available
in AWS Artifact include the Business Associate Addendum (BAA) and the Nondisclosure
Agreement (NDA).

(Q121) Amazon DynamoDB 도 전역 테이블을 시작한다고 했는데 왜 답은 다르지?

(Q122) 필요한 권한을 부여하지 않는 관리형 IAM 정책 해결하는 방법
<b style="color: red;">문의 필요</b>

(Q123) 구성을 담당하는 AWS 책임 분담 모델에 따르면 전적으로 AWS 의 책임이다.

(Q124) Amazon QuickSight 는 클라우드용 구축형 확장 가능한 서버리스의, 임베드 가능 기계 학습 기반 비즈니스 인텔리전스 (BI) 서비스이다. QuickSight 를 사용하면 머신 러닝 기반 Insights 가 포함된 대화형 BI 대시보드를 손쉽게 생성 및 게시할 수 있다.

(Q125) 회사는 AWS IAM 계정 암호 정책을 사용해서 암호 복잡성을 구성할 수 있다.
<b style="color: red;">답이 C가 아닐까</b>

(Q126) AWS 보안 그룹은 인스턴스에 대한 인바운드 및 아웃바운드 트래픽을 제어하는 가상 방화벽 역할을 한다. 각 보안 그룹에 대해 인스턴스에 대한 인바운드 트래픽을 제어하는 규칙과 아웃바운드 트래픽을 제어하는 별도의 규칙 세트를 추가한다.

(Q127) dDDos (Distributed Denial of Service) 완화 기능이 있는 서비스는 Amazon CloudFront, AWS WAF (웹 어플리케이션 방화벽) 이다.

(Q128) SQL 삽입 또는 교차 사이트 스크립팅으로부터 웹 사이트를 보호하려고 한다. 사용해야 하는 서비스는 AWS WAF 이다.

(Q129) 사용자가 비용을 절감 할 수 있도록 Amazon EC2 인스턴스, Amazon Elastic Block Store
(Amazon EBS) 볼륨 및 Amazon RDS 데이터베이스와 같은 AWS 리소스의 크기를
조정하기위한 권장 사항을 제공하는 AWS 서비스는 무엇입니까?
- AWS Trusted Advisor
https://aws.amazon.com/ko/blogs/korea/10-things-you-can-do-today-to-reduce-aws-costs/

(Q130) AWS 클라우드와 프레미스 총 소유 비용을 비교할 때
<b style="color: red;">문의 필요</b>

(Q131) 온프레미스와 클라우드 컴퓨팅의 이점 비교
- 확장성이 탁월하고 비용을 절감하며 차세대 기술을 활용할 수 있도록 지원합니다.

(Q132) 결제 프로세스를 단순화하고 통합하기 위한 AWS 서비스
You can use the consolidated billing feature in AWS Organizations to consolidate billing and
payment for multiple AWS accounts or multiple Amazon Internet Services Pvt. Ltd (AISPL)
accounts. Every organization in AWS Organizations has a master (payer) account that pays
the charges of all the member (linked) accounts.

(Q133) 다음 중 AWS 의 완전 관리형 그래프 데이터베이스 서비스는 Amazon Neptune 이다.

(Q134) 사용자는 PCI DSS(Payment Card Industry Data Security Standard) 를 준수하는 AWS 서비스를 입증해야 한다. 이 요구사항을 충족하기 위해 어떤 AWS 리소스를 사용할 수 있나?
PCI DSS 규정 준수 증명 (AOC) 및 책임 요약은 AWS 규정 준수 보고서에 대한 온 디맨드 액세스를 제공하는 셀프 서비스 포털인 AWS Artifact 를 통해 고객에게 제공된다.

(Q135) 여러 AWS 계정의 효과적인 비용 관리를 허용하는 AWS 서비스는 AWS Organizations 이다.

(Q136) AWS 모범 사례
<b style="color: red;">문의 필요</b>

(Q137) 회사에서 AWS의 VPC로 애플리케이션을 마이그레이션하려고 합니다. 이러한
애플리케이션은 온 프레미스 리소스에 액세스해야 합니다. 회사가 이 목표를 달성할 수 있는
행동 조합은 무엇입니까? (TWO 선택)
A. AWS 서비스 카탈로그를 사용하여 마이그레이션할 수 있는 온 프레미스 리소스 목록을
식별하십시오.
B. 새 VPC에서 온-프레미스 장치와 가상 프라이빗 게이트웨이 간의 VPN 연결을 구축합니다
C. Amazon Athena를 사용하여 온 프레미스 데이터베이스 서버에서 데이터를 쿼리
D. AWS Direct Connect를 사용하여 회사의 온 프레미스 데이터 센터를 AWS에 연결
E. Amazon CloudFront를 활용하여 회사의 온 프레미스 웹 서버를 통해 제공되는 정적 웹
컨텐츠에 대한 액세스를 제한
<b style="color: red;">문의 필요</b>

(Q138) 가용 영역은 각 리전 내에 있는 여러 격리된 위치입니다.

(Q139) AWS 책임 분담 모델에 따라 AWS Cloud 에서 고객의 책임은 어떤 활동입니까?
Amazon Elastic Compute Cloud (Amazon EC2) 같은 서비스는 IaaS(Infrastructure as a Service) (세번째문단 '고객책임', 3번쨰 문장)로 분류되고 고객이 필요한 모든 보안 구성 및 관리 작업을 수행하도록 요구합니다. Amazon EC2 인스턴스를 배포하는 고객은 게스트 운영 체제의 관리(업데이트, 보안 패치 등), 고객이 인스턴스에 설치한 모든 애플리케이션 소프트웨어 또는 유틸리티의 관리, 인스턴스별로 AWS에서 제공한 방화벽(보안 그룹이라고 부름)의 구성 관리에 대한 책임이 있습니다.
<b style="color: red;">이러면 답은 C가 아닐까</b>

(Q140) 회사는 온 프레미스 데이터 센터에서 AWS 클라우드로 마이그레이션하고 있으며 프로젝트에
대한 실질적인 도움을 찾고 있습니다.
회사는 어떻게 이 지원을 받을 수 있습니까? (TQO를 선택하십시오.)
A. 회사의 AWS 계정으로 마이그레이션을 수행하기 위해 AWS Marketplace 팀에 견적을
요청하십시오.
B. AWS Support에 문의하여 사례를 열어 도움을 요청하십시오
C. AWS 전문 서비스를 사용하여 회사의 AWS 계정에서 AWS 랜딩 존을 제공 및 설정
D. AWS 파트너 네트워크 (APN)에서 파트너를 선택하여 마이그레이션을 지원합니다.
E. Amazon Connect를 사용하여 AWS 클라우드로 마이그레이션 할 때 수출 지원을위한
새로운 제안 요청 (RFP) 생성
<b style="color: red;">놀랍게도 C가 없다. 문의 필요</b>

(Q141) 회사는 온 프레미스에서 AWS 클라우드로 마이그레이션 할 계획이다. AWS 툴 또는 서비스가 마이그레이션 후 예상 비용 절감에 대한 자세한 보고서를 제공할 때?
예산 관련 내용이니까 C라고 생각한다.

(Q142) AWS 책임 분담 모델에 따라 고객 책임에는 다음 중 어떤 하나가 포함되나?
위에 말했듯 운영 체제, 네트워크 및 방화벽 구성

(Q143) 안정성을 높이는데 도움이 되는 AWS 클라우드 설계 원칙
안전성 - 전반적인 효율성 측정과 장애로부터 자동 복구

(Q144) SOC 1 보고서와 같은 AWS 규정 준수 문서의 위치
AWS Artifact 를 통해 AWS 고객에게 제공된다.

(Q145) SQL 주입 공격을 방지하기 위해선 AWS WAF 가 사용된다.

(Q146) 보안 그룹은 Amazon Elastic Computer Cloud (Amazon EC2) 인스턴스 보안과 관련하여 어떤 기능을 제공하나?
Amazon EC2 인스턴스에 대한 가상 방화벽 역할을 한다.
AWS Security Groups act like a firewall for your Amazon EC2 instances controlling both
inbound and outbound traffic. When you launch an instance on Amazon EC2, you need to
assign it to a particular security group.
After that, you can set up ports and protocols, which remain open for users and computers
over the internet.
AWS Security Groups are very flexible. You can use the default security group and still
customize it according to your liking (although we don't recommend this practice because
groups should be named according to their purpose.) Or you can create a security group that
you want for your specific applications. To do this, you can write the corresponding code or
use the Amazon EC2 console to make the process easier.

(Q147) 한 회사에서 Amazon Elastic Compute Cloud (Amazon EC2) 를 사용하여 글로벌 상용 어플리케이션을 배포하려고 한다. 배포 솔루션은 최고의 중복성과 내결함성을 갖도록 구축되어야 한다. 어떤 상황에 따라 Amazon EC2 인스턴스를 배포해야 하나?
<b style="color: red;">문의 필요</b>

(Q148) 시스템이 상호 의존성을 줄여야 한다고 명시하는 AWS 클라우드 아키텍쳐 원칙은 무엇인가?
<b style="color: red;">문의 필요</b>

(Q149) 하나 이상의 인스턴스에 대한 트래픽을 제어하기 위한 가상 방화벽 역할을 하는 것은 보안 그룹이다.

(Q150) 고 가용성 어플리케이션을 설계할 때 따라야 할 핵심 원칙 중 하나
<b style="color: red;">문의 필요</b>
일단 모든 구성 요소를 설계한다는 D는 제외한다.