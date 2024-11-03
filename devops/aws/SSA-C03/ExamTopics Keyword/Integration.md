**S3 Transfer Acceleration**
- 설명: S3 Transfer Acceleration은 Amazon S3에 파일을 업로드하고 다운로드할 때 전송 속도를 높이는 기능으로, AWS 글로벌 네트워크를 통해 트래픽을 라우팅합니다. 
  - 사용 사례: 대용량 파일을 업로드할 때나 여러 지역에서 데이터를 업로드하는 사용자에게 유용합니다. 지연 시간을 줄이고 전송 속도를 개선합니다.

**Amazon Redshift, Amazon Athena, AWS Glue, Amazon EMR, Apache Spark Cluster**
- Amazon Redshift: 대규모 데이터 분석을 위한 완전 관리형 데이터 웨어하우스 서비스입니다.
  - 사용 사례: OLAP(온라인 분석 처리) 및 대규모 데이터 분석에 적합합니다.
- Amazon Athena: S3에 저장된 데이터를 SQL을 사용해 분석할 수 있게 해주는 대화형 쿼리 서비스입니다.
  - 사용 사례: S3에 저장된 데이터에 대한 즉석 쿼리와 분석에 적합합니다.
- AWS Glue: 데이터 분석을 위해 데이터를 준비하는 완전 관리형 ETL(추출, 변환, 적재) 서비스입니다.
  - 사용 사례: 데이터 준비 및 카탈로그 자동화에 유용하며, 데이터 레이크에 적합합니다.
- Amazon EMR (Elastic MapReduce): Apache Hadoop 및 Apache Spark와 같은 빅데이터 프레임워크를 쉽게 실행할 수 있는 관리형 클러스터 플랫폼입니다.
  - 사용 사례: 대량의 데이터를 빠르게 처리할 때 유용하며, 로그 분석, 데이터 변환, 기계 학습 작업 등에 사용됩니다.
- Apache Spark Cluster: 대규모 데이터 처리를 위한 통합 분석 엔진으로, 스트리밍, SQL, 기계 학습 및 그래프 처리 모듈이 내장되어 있습니다.
  - 사용 사례: 대규모 데이터 작업을 위한 인메모리 데이터 처리가 필요할 때 사용되며, EMR과 함께 자주 사용됩니다.

**AWS Cloud Trail**
- 설명: AWS CloudTrail은 AWS 계정의 거버넌스, 준수 및 운영 및 리스크 감사 기능을 제공하는 서비스입니다. 
  - 사용 사례: AWS 인프라 전반에서 사용자 활동 및 API 사용을 추적하여 준수 및 보안 요구 사항을 충족하는 데 사용됩니다.

**Gateway VPC Endpoint**
- 설명: Gateway VPC Endpoint는 인터넷 게이트웨이, NAT 장치, VPN 연결 또는 AWS Direct Connect 연결 없이 VPC와 AWS 서비스 간의 비공식적 연결을 제공합니다. 
  - 사용 사례: S3 및 DynamoDB에 안전하게 접근할 때 유용하며, 인터넷에 데이터를 노출하지 않고 사용할 수 있습니다.

**Amazon EFS**
- 설명: AWS 클라우드 서비스와 온프레미스 리소스와 함께 사용할 수 있는 확장 가능하고 완전 관리형 파일 저장 서비스입니다. 
  - 사용 사례: 콘텐츠 관리 시스템, 웹 서버, 빅데이터 애플리케이션 등 파일 공유가 필요한 경우에 적합합니다.

**AWS Snowball Edge, S3 File Gateway**
- AWS Snowball Edge: 대량의 데이터를 AWS로 이동하기 위한 저장 및 컴퓨팅 기능을 갖춘 데이터 전송 장치입니다.
  - 사용 사례: 대규모 데이터 마이그레이션 시 유용하며, 대역폭이 제한된 상황에서 사용됩니다.

- S3 File Gateway: 온프레미스 애플리케이션이 Amazon S3 저장소에 파일 인터페이스를 통해 접근할 수 있게 해주는 서비스입니다.
  - 사용 사례: 하이브리드 클라우드 스토리지에서 S3에 데이터를 저장하면서 표준 파일 프로토콜을 통해 접근할 필요가 있을 때 유용합니다.

**Amazon Kinesis Data Analytics, Amazon Kinesis Data Streams, Amazon Simple Queue Service (Amazon SQS), Amazon Simple Notification Service (Amazon SNS)**
- Amazon Kinesis Data Analytics: SQL을 사용해 스트리밍 데이터를 실시간으로 처리하고 분석할 수 있게 해주는 서비스입니다.
  - 사용 사례: 스트리밍 데이터에 대한 실시간 분석이 필요할 때 유용합니다.

- Amazon Kinesis Data Streams: 실시간 스트리밍 데이터를 수집, 처리 및 분석할 수 있게 해주는 서비스입니다.
  - 사용 사례: 시스템 로그 모니터링, 이벤트 처리와 같은 실시간 애플리케이션 구축에 적합합니다.

- Amazon SQS (Simple Queue Service): 마이크로서비스, 분산 시스템 및 서버리스 애플리케이션의 분리를 가능하게 하는 완전 관리형 메시지 큐 서비스입니다.
  - 사용 사례: 애플리케이션 구성 요소 간의 신뢰성 있는 통신을 보장하기 위해 메시지를 큐잉할 때 사용됩니다.

- Amazon SNS (Simple Notification Service): 구독하는 엔드포인트나 클라이언트에 메시지를 전달할 수 있게 해주는 완전 관리형 게시/구독 메시징 서비스입니다.
  - 사용 사례: 분산 시스템에 알림과 메시지를 보내거나 워크플로를 트리거하는 데 유용합니다.

**Auto Scaling, Amazon Event Bridge**
- Auto Scaling: 트래픽 패턴이나 예약된 시간에 따라 EC2 인스턴스 수를 자동으로 조정하는 서비스입니다.
  - 사용 사례: 성능을 유지하고 비용을 최소화하기 위해 리소스를 필요에 따라 확장하거나 축소할 때 유용합니다.

- Amazon EventBridge: 이벤트를 사용하여 애플리케이션을 연결할 수 있게 해주는 서버리스 이벤트 버스 서비스입니다.
  - 사용 사례: 이벤트 기반 아키텍처 구축에 유용하며, 서비스가 AWS 서비스 간의 변화 및 이벤트에 응답할 수 있게 합니다.

**AWS Data Sync, S3 Glocier Deep Archive, S3 Cluster Flexible Retrieval**
- AWS DataSync: 온프레미스 저장소와 AWS 저장 서비스 간의 데이터 전송을 단순화하고 자동화하며 가속화하는 데이터 전송 서비스입니다.
  - 사용 사례: 자동화된 데이터 마이그레이션 및 복제 작업에 적합합니다.

- S3 Glacier Deep Archive: 드물게 접근되는 데이터를 위한 저비용 저장 클래스이며 장기 아카이빙을 위해 설계되었습니다.
  - 사용 사례: 데이터 검색이 드문 경우의 컴플라이언스 및 아카이브 용도로 적합합니다.

- S3 Intelligent-Tiering: 데이터 접근 패턴의 변화에 따라 데이터를 가장 비용 효율적인 저장 계층으로 자동 이동시키는 S3 저장 클래스입니다.
  - 사용 사례: 접근 패턴이 불확실하거나 예측할 수 없는 데이터에 적합하여 비용을 최적화하면서 성능을 유지합니다.

**Amazon API Gateway REST API**
- 설명: Amazon API Gateway는 RESTful API를 생성, 배포 및 관리할 수 있게 해주는 서비스입니다. 
  - 사용 사례: 백엔드 서비스와의 통신을 위한 API를 쉽게 만들고, 사용자 인증 및 모니터링을 지원할 수 있습니다.

**AWS Secrets Manager, AWS Systems Manager Parameter Store, AWS Key Management Service (AWS KMS), Amazon Elastic Block Store (Amazon EBS)**
- AWS Secrets Manager: 비밀번호 및 API 키와 같은 비밀 정보를 안전하게 저장하고 관리할 수 있게 해주는 서비스입니다.
  - 사용 사례: 애플리케이션에서 사용하는 데이터베이스 비밀번호를 안전하게 관리하고 자동으로 갱신할 수 있습니다.

- AWS Systems Manager Parameter Store: 애플리케이션 설정 값 및 비밀 정보를 안전하게 저장하고 관리하는 서비스입니다.
  - 사용 사례: 환경 변수나 구성 정보를 중앙에서 관리하고, 필요할 때 안전하게 조회할 수 있습니다.

- AWS Key Management Service (AWS KMS): 데이터 암호화를 위한 키를 생성하고 관리하는 서비스입니다.
  - 사용 사례: 데이터 보호를 위한 키 관리, 암호화 및 복호화에 사용됩니다.

- Amazon Elastic Block Store (Amazon EBS): EC2 인스턴스에 대한 블록 스토리지 서비스를 제공합니다.
  - 사용 사례: 데이터베이스와 같은 애플리케이션에 필요한 영구 저장소로 사용됩니다.

**Application Load Balancer (ALB), Route 53, CloudFront**
- Application Load Balancer (ALB): 애플리케이션 계층에서 HTTP/HTTPS 트래픽을 분산하는 로드 밸런서입니다.
  - 사용 사례: 웹 애플리케이션의 트래픽을 여러 EC2 인스턴스로 분산하여 가용성과 성능을 향상시킵니다.

- Route 53: AWS의 도메인 이름 시스템(DNS) 웹 서비스입니다.
  - 사용 사례: 도메인 이름을 관리하고, 사용자 요청을 가장 가까운 리전으로 라우팅하여 지연 시간을 줄입니다.

- CloudFront: AWS의 콘텐츠 전송 네트워크(CDN) 서비스입니다.
  - 사용 사례: 정적 및 동적 콘텐츠를 전 세계적으로 빠르게 전송하여 사용자 경험을 개선합니다.

**Configure Systems Manager, Amazon EventBridge**
- Configure Systems Manager: AWS Systems Manager의 기능으로, 인프라 구성을 관리하고 설정할 수 있습니다.
  - 사용 사례: EC2 인스턴스의 패치 관리 및 구성 상태를 모니터링합니다.

- Amazon EventBridge: 이벤트 기반 아키텍처를 구축하는 데 사용되는 서버리스 이벤트 버스입니다.
  - 사용 사례: 다양한 AWS 서비스와 애플리케이션 간의 이벤트를 쉽게 전달하고 처리합니다.

**Amazon GuardDuty, AWS Network Firewall, AWS Firewall Manager**
- Amazon GuardDuty: AWS 환경에서 비정상적인 활동을 모니터링하고 보안 위협을 탐지하는 서비스입니다.
  - 사용 사례: AWS 계정 및 리소스에 대한 보안 감시와 위협 탐지에 사용됩니다.

- AWS Network Firewall: VPC의 네트워크 트래픽을 보호하는 관리형 방화벽 서비스입니다.
  - 사용 사례: VPC 내에서 트래픽을 필터링하고, 보안 규칙을 적용하여 네트워크를 보호합니다.

- AWS Firewall Manager: AWS 환경에서 방화벽 규칙을 중앙에서 관리하는 서비스입니다.
  - 사용 사례: 여러 AWS 계정 및 리전에서 방화벽 정책을 일관되게 적용하고 관리합니다.

**Amazon QuickSight**
- 설명: Amazon QuickSight는 클라우드 기반의 BI(Business Intelligence) 서비스로, 데이터를 시각화하고 분석할 수 있게 해줍니다. 
  - 사용 사례: 대시보드 및 보고서를 생성하여 비즈니스 데이터를 쉽게 이해하고 인사이트를 도출할 수 있습니다.

**Amazon Marketplace**
- 설명: AWS에서 제공하는 마켓플레이스로, 서드파티 소프트웨어 및 서비스에 접근할 수 있게 해줍니다. 
  - 사용 사례: 기업이 AWS 인프라와 통합하여 다양한 애플리케이션 및 서비스를 탐색하고 구매할 수 있습니다.

**Application Load Balancer, Amazon Elastic Kubernetes Service (Amazon EKS), Kubernetes Cluster Autoscaler**
- Application Load Balancer (ALB): 앞서 설명한 대로, HTTP/HTTPS 트래픽을 분산합니다.

- Amazon Elastic Kubernetes Service (Amazon EKS): Kubernetes 클러스터를 관리할 수 있게 해주는 완전 관리형 서비스입니다.
  - 사용 사례: Kubernetes를 사용하여 컨테이너화된 애플리케이션을 쉽게 배포하고 관리합니다.

- Kubernetes Cluster Autoscaler: 클러스터의 리소스를 자동으로 조정하는 도구입니다.
  - 사용 사례: 워크로드 변화에 따라 클러스터의 노드를 자동으로 추가하거나 제거하여 비용 효율성을 높입니다.

**S3 Standard, S3 Intelligent-Tiering, S3 Standard-Infrequent Access (S3 Standard-IA), S3 One Zone-Infrequent Access (S3 One Zone-IA)**
- S3 Standard: 빈번하게 접근되는 데이터를 위한 저장 클래스입니다.
  - 사용 사례: 웹 사이트의 이미지나 동영상과 같이 자주 사용하는 데이터를 저장합니다.

- S3 Intelligent-Tiering: 데이터 접근 패턴에 따라 자동으로 저장 계층을 조정합니다.
  - 사용 사례: 예측할 수 없는 데이터 접근 패턴을 가진 데이터에 적합합니다.

- S3 Standard-Infrequent Access (S3 Standard-IA): 자주 사용되지 않지만 즉시 필요할 수 있는 데이터에 적합한 저장 클래스입니다.
  - 사용 사례: 오래된 백업 파일과 같이 가끔 접근되는 데이터를 저장합니다.

- S3 One Zone-Infrequent Access (S3 One Zone-IA): 단일 가용 영역에 저장되며, 낮은 비용으로 자주 접근하지 않는 데이터를 저장합니다.
  - 사용 사례: 재해 복구를 고려하지 않는 비즈니스 데이터 저장에 유용합니다.

**S3 Standard to S3 Glacier Deep Archive**
- 설명: S3 Standard에서 S3 Glacier Deep Archive로의 전환은 데이터를 저비용 장기 아카이브 저장소로 이동하는 것입니다. 
  - 사용 사례: 데이터가 더 이상 자주 필요하지 않지만 보존해야 하는 경우, 예를 들어 규제 준수를 위해 아카이브해야 하는 데이터에 적합합니다.

**Amazon DynamoDB Provision, DynamoDB Accelerator (DAX)**
- DynamoDB Provision: DynamoDB에서 요구 사항에 따라 읽기 및 쓰기 용량을 미리 예약하는 기능입니다.
  - 사용 사례: 예측 가능한 트래픽 패턴을 가진 애플리케이션에서 성능을 보장할 수 있습니다.

- DynamoDB Accelerator (DAX): DynamoDB의 인메모리 캐시로, 초당 수천 건의 요청을 처리할 수 있도록 지원합니다.
  - 사용 사례: 지연 시간이 짧은 데이터 접근이 필요한 애플리케이션에서 성능을 향상시킵니다.

**Bastion Server**
- 설명: 보안성이 높은 네트워크에 접근하기 위한 중계 서버입니다. 
  - 사용 사례: 관리자가 내부 리소스에 안전하게 접근할 수 있도록 SSH를 통해 보안 연결을 제공합니다.

**AWS Single Sign-On (AWS SSO), Identity Provider (IdP)**
- AWS Single Sign-On (AWS SSO): 여러 AWS 계정과 비즈니스 애플리케이션에 대한 단일 로그인을 제공하는 서비스입니다.
  - 사용 사례: 사용자가 여러 애플리케이션에 대한 액세스를 쉽게 관리할 수 있도록 지원합니다.

- Identity Provider (IdP): 사용자 인증 및 ID 관리를 제공하는 시스템입니다.
  - 사용 사례: AWS와 외부 애플리케이션 간의 사용자 인증을 통합하여 관리합니다.

**Voice over Internet Protocol (VoIP), Network Load Balancer (NLB), Application Load Balancer (ALB)**
- Voice over Internet Protocol (VoIP): 인터넷을 통해 음성 통신을 가능하게 하는 기술입니다.
  - 사용 사례: 음성 통화를 인터넷으로 전송하여 전화 서비스의 비용을 줄입니다.

- Network Load Balancer (NLB): TCP/UDP 트래픽을 효율적으로 분산하는 로드 밸런서입니다.
  - 사용 사례: 고성능 네트워크 트래픽을 처리하고, 지연 시간을 최소화합니다.

- Application Load Balancer (ALB): 앞서 설명한 대로 HTTP/HTTPS 트래픽을 분산합니다.

**AWS Config, Cost Explorer**
- AWS Config: AWS 리소스의 구성 및 변경 사항을 추적하는 서비스입니다.
  - 사용 사례: 리소스의 변경 이력을 모니터링하고 규정 준수를 관리합니다.

- Cost Explorer: AWS 사용량 및 비용을 시각적으로 분석할 수 있는 도구입니다.
  - 사용 사례: 비용 사용 패턴을 이해하고 최적화하는 데 유용합니다.

**AWS Fargate**
- 설명: 컨테이너를 실행할 수 있는 서버리스 컴퓨팅 엔진으로, 인프라 관리 없이 애플리케이션을 배포할 수 있게 해줍니다. 
  - 사용 사례: Kubernetes 또는 Amazon ECS에서 컨테이너를 간편하게 배포하고 관리할 수 있습니다.

**Amazon Kinesis Data Firehose, Amazon Kinesis Data Streams**
- Amazon Kinesis Data Firehose: 실시간으로 데이터를 수집하고, 변환하고, 저장하는 완전 관리형 서비스입니다.
  - 사용 사례: 데이터 분석을 위한 S3 또는 Redshift로 데이터를 쉽게 전송합니다.

- Amazon Kinesis Data Streams: 실시간 스트리밍 데이터를 수집하고 처리하는 서비스입니다.
  - 사용 사례: 이벤트 기반 애플리케이션 및 데이터 스트리밍 처리에 사용됩니다.

**AWS CloudTrail**
- 설명: AWS 계정의 API 호출을 기록하고 모니터링하는 서비스입니다. 
  - 사용 사례: 보안 감사를 위해 AWS 환경의 변경 이력을 추적합니다.

**Amazon GuardDuty, Amazon Inspector, AWS Shield**
- Amazon GuardDuty: AWS 환경에서 비정상적인 활동을 모니터링하고 보안 위협을 탐지하는 서비스입니다.

- Amazon Inspector: 애플리케이션 보안을 평가하고 취약점을 찾아주는 서비스입니다.
  - 사용 사례: 보안 위험을 사전에 식별하고 관리하여 시스템의 안전성을 높입니다.

- AWS Shield: DDoS 공격으로부터 AWS 리소스를 보호하는 서비스입니다.
  - 사용 사례: 애플리케이션을 DDoS 공격으로부터 보호하여 가용성을 유지합니다.

**Provisioned IOPS SSD**
- 설명: 고성능의 SSD 스토리지로, 미리 예약된 IOPS(입출력 작업 수)를 제공합니다. 
  - 사용 사례: 데이터베이스와 같이 높은 성능과 일관성을 요구하는 애플리케이션에 적합합니다.

**Amazon OpenSearch Service (Amazon Elasticsearch Service)**
- 설명: 로그 분석, 검색 및 분석을 위한 관리형 검색 서비스입니다. 
  - 사용 사례: 대규모 데이터 세트를 실시간으로 검색하고 분석하는 데 사용됩니다.

**Amazon AppFlow, Amazon Elastic Container Service**
- Amazon AppFlow: 클라우드 애플리케이션 간의 데이터 흐름을 자동화하는 서비스입니다.
  - 사용 사례: Salesforce와 같은 SaaS 애플리케이션 간에 데이터를 쉽게 전송합니다.

- Amazon Elastic Container Service (ECS): Docker 컨테이너를 쉽게 실행하고 관리할 수 있도록 돕는 서비스입니다.
  - 사용 사례: 컨테이너화된 애플리케이션을 배포하고 확장하는 데 유용합니다.

**NAT Gateway**
- 설명: VPC에서 인터넷에 연결된 리소스가 외부와 통신할 수 있도록 해주는 서비스입니다. 
  - 사용 사례: 프라이빗 서브넷에서 실행되는 인스턴스가 인터넷에 접근할 수 있도록 합니다.

**AWS Management Console**
- 설명: AWS 리소스를 관리할 수 있는 웹 기반 인터페이스입니다. 
  - 사용 사례: AWS 서비스의 배포, 구성 및 모니터링을 용이하게 합니다.

**MFA (Multi-Factor Authentication)**
- 설명: 사용자 인증의 보안을 강화하기 위해 두 가지 이상의 인증 요소를 요구하는 방식입니다. 
  - 사용 사례: AWS 계정의 보안을 강화하여 무단 접근을 방지합니다.

**Personally Identifiable Information (PII)**
- 설명: 개인을 식별할 수 있는 정보를 의미합니다. 
  - 사용 사례: 데이터 보안 및 프라이버시 정책에 따라 PII를 안전하게 관리해야 합니다.

**Amazon Elastic File System (Amazon EFS)**
- 설명: AWS 클라우드 서비스와 온프레미스 리소스 간에 공유 가능한 파일 스토리지 서비스입니다. 
  - 사용 사례: 여러 EC2 인스턴스에서 동시에 접근해야 하는 파일 저장에 적합합니다.

**Amazon S3 Glacier Instant Retrieval, Amazon S3 Intelligent-Tiering**
- Amazon S3 Glacier Instant Retrieval: 아카이브 데이터에 대한 빠른 접근을 제공하는 저장 클래스입니다.
  - 사용 사례: 드물게 사용되지만 즉시 필요한 데이터 아카이빙에 적합합니다.

- Amazon S3 0Intelligent-Tiering: 접근 패턴에 따라 데이터를 자동으로 저장 계층으로 이동하는 기능을 제공합니다.
  - 사용 사례: 데이터 접근 패턴이 불확실한 경우에 비용을 최적화합니다.

**AWS Systems Manager Patch Manager**
- 설명: AWS 리소스의 소프트웨어 패치를 자동으로 관리하고 적용하는 서비스입니다. 
  - 사용 사례: 보안 및 성능을 유지하기 위해 EC2 인스턴스의 패치를 자동화합니다.

**Amazon Kinesis Data Firehose, Amazon Simple Email Service (Amazon SES)**
- Amazon Kinesis Data Firehose: 앞서 설명한 대로 실시간 데이터 수집 및 전송 서비스를 제공합니다.

- Amazon Simple Email Service (SES): 이메일을 쉽게 보내고 받을 수 있는 관리형 서비스입니다.
  - 사용 사례: 대량 이메일 발송 및 수신을 위한 비용 효율적인 솔루션을 제공합니다.

**Elastic Kubernetes Service (Amazon EKS), Amazon Elastic Block Store (Amazon EBS)**
- Elastic Kubernetes Service (Amazon EKS): Kubernetes 클러스터를 쉽게 관리할 수 있도록 도와주는 서비스입니다.

- Amazon Elastic Block Store (Amazon EBS): EC2 인스턴스에 대한 블록 스토리지 서비스를 제공합니다.

**S3 One Zone-Infrequent Access (S3 One Zone-IA)**
- 설명: 단일 가용 영역에 저장된 저비용 저장 클래스입니다. 
  - 사용 사례: 가끔 접근하는 데이터에 적합하며, 비용을 절감할 수 있습니다.

**AWS Certificate Manager (ACM)**
- 설명: SSL/TLS 인증서를 쉽게 관리하고 배포할 수 있는 서비스입니다. 
  - 사용 사례: 웹 애플리케이션의 보안을 강화하기 위해 HTTPS를 설정하는 데 사용됩니다.

**Amazon Comprehend, Amazon Rekognition, Amazon SageMaker**
- Amazon Comprehend: 자연어 처리(NLP) 서비스로, 텍스트에서 인사이트를 추출합니다.
  - 사용 사례: 고객 피드백 분석 및 텍스트 분류에 사용됩니다.

- Amazon Rekognition: 이미지 및 비디오 분석을 위한 서비스입니다.
  - 사용 사례: 얼굴 인식 및 객체 감지와 같은 기능에 사용됩니다.

- Amazon SageMaker: 기계 학습 모델을 쉽게 구축, 훈련 및 배포할 수 있게 해주는 서비스입니다.
  - 사용 사례: 데이터 과학자가 모델을 개발하고 프로덕션 환경에 배포할 수 있도록 지원합니다.

**Amazon Machine Image (AMI)**
- 설명: EC2 인스턴스를 시작하는 데 필요한 모든 정보를 포함하는 템플릿입니다. 
  - 사용 사례: 애플리케이션의 배포 및 복구를 용이하게 하는 기본 이미지로 사용됩니다.

**Amazon CloudFront, Amazon Kinesis Data Streams**
- Amazon CloudFront: 앞서 설명한 대로 콘텐츠 전송 네트워크 서비스입니다.

- Amazon Kinesis Data Streams: 앞서 설명한 대로 실시간 데이터 스트리밍 서비스입니다.

**Application Load Balancer (ALB), Server Name Indication (SNI)**
- Application Load Balancer (ALB): 앞서 설명한 대로 HTTP/HTTPS 트래픽을 분산합니다.

- Server Name Indication (SNI): SSL/TLS 연결을 설정할 때 클라이언트가 연결하려는 서버의 호스트 이름을 제공하는 확장 기능입니다.
  - 사용 사례: 여러 도메인 이름에 대해 단일 IP 주소에서 SSL 인증서를 사용할 수 있도록 합니다.

**Amazon CloudWatch Events, AWS Systems Manager Parameter Store**
- Amazon CloudWatch Events: AWS 리소스 및 애플리케이션 상태를 모니터링하고 이벤트를 관리하는 서비스입니다.

- AWS Systems Manager Parameter Store: 앞서 설명한 대로 애플리케이션 설정 및 비밀 정보를 안전하게 저장하고 관리하는 서비스입니다.

**Certificate Authority (CA)**
- 설명: SSL/TLS 인증서를 발급하고 관리하는 신뢰할 수 있는 기관입니다. 
  - 사용 사례: 웹사이트의 신뢰성을 보장하기 위해 SSL 인증서를 발급합니다.

**AWS Elastic Beanstalk**
- 설명: 애플리케이션을 쉽게 배포하고 관리할 수 있도록 해주는 PaaS 서비스입니다. 
  - 사용 사례: 웹 애플리케이션을 신속하게 배포하고 관리할 수 있는 환경을 제공합니다.

**FSx for Windows File Server, S3 File Gateway, FSx File Gateway**
- FSx for Windows File Server: 완전 관리형 Windows 파일 시스템으로, SMB 프로토콜을 지원합니다.
  - 사용 사례: Windows 환경에서 파일 공유를 위한 스토리지로 사용됩니다.

- S3 File Gateway: 온프레미스 애플리케이션과 Amazon S3 간의 파일 저장소를 연결하는 서비스입니다.
  - 사용 사례: 기존 애플리케이션이 S3에 파일을 저장할 수 있도록 지원합니다.

- FSx File Gateway: Amazon FSx 스토리지를 온프레미스 애플리케이션에 연결하는 서비스입니다.
  - 사용 사례: 온프레미스 데이터와 클라우드 스토리지를 통합하여 효율적으로 관리합니다.

**Protected Health Information (PHI), Amazon Textract, Amazon SageMaker, Amazon Comprehend Medical**
- Protected Health Information (PHI): 개인의 건강 정보로, 보안이 필요합니다.
  - 사용 사례: 의료 데이터 관리 및 보호에 대한 규제를 준수합니다.

- Amazon Textract: 문서에서 데이터를 자동으로 추출하는 서비스입니다.
  - 사용 사례: 스캔한 문서에서 텍스트 및 데이터 구조를 추출하여 처리합니다.

- Amazon SageMaker: 앞서 설명한 대로 기계 학습 모델을 개발할 수 있게 해주는 서비스입니다.

- Amazon Comprehend Medical: 의료 데이터를 분석하여 인사이트를 제공하는 서비스입니다.
  - 사용 사례: 의료 기록 및 환자 피드백에서 정보를 추출합니다.

**S3 One Zone-Infrequent Access (S3 One Zone-IA), S3 Standard-Infrequent Access (S3 Standard-IA)**
- S3 One Zone-Infrequent Access (S3 One Zone-IA): 앞서 설명한 대로 단일 가용 영역에 저장된 저비용 저장 클래스입니다.

- S3 Standard-Infrequent Access (S3 Standard-IA): 앞서 설명한 대로 자주 사용되지 않는 데이터에 적합한 저장 클래스입니다.

**Provision an AWS Direct Connect**
- 설명: AWS와 온프레미스 데이터 센터 간에 전용 네트워크 연결을 설정하는 서비스입니다. 
  - 사용 사례: 안정적이고 빠른 네트워크 연결이 필요한 기업 환경에서 사용됩니다.

**Multi-AZ, Amazon RDS Proxy**
- Multi-AZ: Amazon RDS에서 높은 가용성을 제공하기 위한 구성입니다.
  - 사용 사례: 데이터베이스 인스턴스를 여러 가용 영역에 배포하여 장애 조치를 지원합니다.

- Amazon RDS Proxy: Amazon RDS 데이터베이스에 대한 연결을 관리하여 성능과 가용성을 향상시키는 서비스입니다.
  - 사용 사례: 데이터베이스 연결의 부하를 줄이고, 애플리케이션 성능을 개선합니다.

**Recovery Point Objective (RPO), Recovery Time Objective (RTO)**
- Recovery Point Objective (RPO): 데이터 복구 시점의 최대 허용 시간입니다.
  - 사용 사례: 데이터 손실을 최소화하기 위한 백업 전략을 계획합니다.

- Recovery Time Objective (RTO): 시스템 복구에 필요한 최대 시간을 정의합니다.
  - 사용 사례: 비즈니스 연속성을 확보하기 위한 복구 계획을 수립합니다.

**NAT Gateway**
- 설명: 앞서 설명한 대로 VPC의 프라이빗 서브넷에서 인터넷에 연결하는 서비스입니다.

**Linux-based Bastion Host**
- 설명: Linux 기반의 보안 중계 서버로, 관리자가 내부 네트워크에 안전하게 접근할 수 있게 해줍니다. 
  - 사용 사례: SSH를 통해 안전하게 서버에 접근할 수 있는 환경을 제공합니다.

**Storage Area Network (SAN), AWS DataSync, AWS Database Migration Service**
- Storage Area Network (SAN): 스토리지 장치를 네트워크로 연결하여 데이터 저장 및 관리하는 시스템입니다.
  - 사용 사례: 대규모 데이터 스토리지 솔루션으로 사용됩니다.

- AWS DataSync: 온프레미스 저장소와 AWS 저장 서비스 간의 데이터 전송을 자동화하는 서비스입니다.

- AWS Database Migration Service: 데이터베이스를 AWS로 마이그레이션하는 데 도움을 주는 서비스입니다.
  - 사용 사례: 기존 데이터베이스를 AWS로 간편하게 이전할 수 있도록 지원합니다.

**Amazon Kinesis Data Stream, Amazon Kinesis Data Firehose**
- Amazon Kinesis Data Stream: 앞서 설명한 대로 실시간 데이터 스트리밍 서비스입니다.

- Amazon Kinesis Data Firehose: 앞서 설명한 대로 데이터 수집 및 전송 서비스를 제공합니다.

**AWS Managed Service Provider (MSP), Amazon Machine Image (AMI), AWS Key Management Service (AWS KMS)**
- AWS Managed Service Provider (MSP): AWS 리소스와 서비스를 관리하는 전문 서비스 제공업체입니다.
  - 사용 사례: 기업의 AWS 환경을 관리하고 최적화합니다.

- Amazon Machine Image (AMI): 앞서 설명한 대로 EC2 인스턴스를 시작하는 데 필요한 템플릿입니다.

- AWS Key Management Service (AWS KMS): 앞서 설명한 대로 데이터 암호화를 위한 키를 관리하는 서비스입니다.

**Spot Instance, Reserved Instance, Spot Block, On-Demand Instance**
- Spot Instance: AWS의 잉여 용량을 저렴한 가격에 이용할 수 있는 EC2 인스턴스입니다.
  - 사용 사례: 비용 효율적인 방식으로 비정기적인 워크로드를 처리합니다.

- Reserved Instance: 특정 기간 동안 EC2 인스턴스를 예약하여 비용을 절감하는 옵션입니다.
  - 사용 사례: 예측 가능한 워크로드에 대한 비용을 최적화합니다.

- Spot Block: 정해진 시간 동안 Spot Instance를 예약하는 옵션입니다.
  - 사용 사례: 특정 시간에 필요한 리소스를 사전에 예약하여 예기치 않은 중단을 방지합니다.

- On-Demand Instance: 사용자가 필요할 때마다 EC2 인스턴스를 시작할 수 있는 유연한 옵션입니다.
  - 사용 사례: 예측할 수 없는 워크로드에 적합하며, 필요에 따라 확장할 수 있습니다.

**AWS Systems Manager OpsCenter**
- 설명: AWS 리소스의 운영 문제를 관리하고 해결할 수 있는 서비스입니다. 
  - 사용 사례: 인프라의 상태를 모니터링하고, 문제를 중앙에서 관리합니다.

**S3 Cross-Region Replication**
- 설명: S3 버킷의 데이터를 다른 리전의 S3 버킷으로 자동으로 복제하는 기능입니다. 
  - 사용 사례: 데이터 중복성을 확보하고 재해 복구를 위한 전략으로 사용됩니다.

**RDS Single-AZ DB Instance, Amazon ElastiCache**
- RDS Single-AZ DB Instance: 단일 가용 영역에 배포된 RDS 데이터베이스 인스턴스입니다.
  - 사용 사례: 비용 효율적인 테스트 및 개발 환경에 적합합니다.

- Amazon ElastiCache: 인메모리 캐시 서비스를 제공하여 애플리케이션 성능을 향상시킵니다.
  - 사용 사례: 데이터베이스 쿼리의 응답 시간을 줄이고, 높은 성능을 요구하는 애플리케이션에 사용됩니다.

**Multi-AZ Aurora Replicas**
- 설명: Amazon Aurora의 고가용성 및 자동 장애 조치를 위한 복제본입니다. 
  - 사용 사례: 데이터베이스의 성능을 향상시키고 가용성을 높입니다.

**Amazon EMR**
- 설명: 빅데이터 처리 및 분석을 위한 관리형 클러스터 서비스입니다. 
  - 사용 사례: 대규모 데이터 처리 작업을 쉽게 실행하고 관리합니다.

**Lustre**
- 설명: 고성능 컴퓨팅(HPC) 워크로드를 지원하는 분산 파일 시스템입니다. 
  - 사용 사례: 데이터 집약적인 애플리케이션 및 과학적 계산에 사용됩니다.

1. Amazon Elastic File System (Amazon EFS)
설명: 확장성이 뛰어난 서버리스 파일 스토리지 서비스로, EC2 인스턴스와 온프레미스 리소스에서 사용할 수 있습니다.
예시: 여러 EC2 인스턴스가 동시에 EFS에 저장된 데이터를 공유하는 웹 애플리케이션.

2. AWS DataSync
설명: 온프레미스 스토리지와 AWS 간의 데이터 전송을 자동화하고 가속화하는 서비스입니다.
예시: 대량의 파일을 온프레미스 NAS에서 S3로 정기적으로 전송하는 작업.

3. Amazon Elastic Block Store (Amazon EBS)
설명: EC2 인스턴스에 연결할 수 있는 블록 레벨 스토리지입니다.
예시: EC2 인스턴스의 데이터베이스를 위한 EBS 볼륨 생성.

4. AWS Glue ETL
설명: 데이터 추출, 변환 및 로딩(ETL) 작업을 자동화하고 관리하는 서비스입니다.
예시: S3의 CSV 파일을 정제하여 Redshift에 로드하는 ETL 작업.

5. Job Bookmarks
설명: AWS Glue ETL 작업의 중단 지점을 기록하여 재처리 시 중복을 피하도록 돕는 기능입니다.
예시: 대량의 데이터가 처리된 후 다음 ETL 실행 시 처리한 지점을 기억함.

6. AWS Shield Advanced
설명: DDoS 공격으로부터 애플리케이션을 보호하는 관리형 서비스입니다.
예시: 웹 애플리케이션의 공격을 감지하고 방어하는 데 사용됩니다.

7. Amazon GuardDuty
설명: AWS 계정 및 워크로드에 대한 위협 탐지 서비스입니다.
예시: 비정상적인 API 호출 패턴을 감지하여 경고를 발생.

8. Resource-based policy
설명: 특정 리소스에 대한 접근 권한을 정의하는 정책으로, IAM 사용자와 역할 외에도 적용됩니다.
예시: S3 버킷에 대해 특정 IAM 역할에 접근 권한을 부여하는 정책.

9. Server-side encryption with customer-provided keys (SSE-C)
설명: 고객이 제공하는 암호화 키를 사용하여 데이터를 S3에 저장할 때 암호화하는 방법입니다.
예시: 사용자가 암호화 키를 제공하여 S3 객체를 암호화하는 경우.

10. Server-side encryption with Amazon S3 managed keys (SSE-S3)
설명: Amazon S3가 관리하는 키를 사용하여 데이터를 자동으로 암호화하는 방법입니다.
예시: S3에 업로드하는 모든 파일이 자동으로 SSE-S3로 암호화됨.

11. Server-side encryption with AWS KMS keys (SSE-KMS)
설명: AWS Key Management Service (KMS)로 관리되는 키를 사용하여 데이터를 암호화하는 방법입니다.
예시: S3 객체를 KMS 키로 암호화하여 보다 세부적인 권한 관리.

12. Amazon QuickSight with Amazon Redshift
설명: Amazon Redshift에 저장된 데이터를 시각화하고 분석하는 BI 도구입니다.
예시: Redshift 데이터베이스에서 판매 데이터를 가져와 대시보드를 만드는 작업.

13. ActiveMQ
설명: 오픈 소스 메시지 브로커로, JMS(Java Message Service)를 지원합니다.
예시: 다양한 애플리케이션 간 메시지를 전송하고 수신하는 데 사용.

14. Amazon Elastic Container Service (Amazon ECS)
설명: Docker 컨테이너를 쉽게 실행, 관리할 수 있는 클라우드 서비스입니다.
예시: 여러 개의 컨테이너화된 마이크로서비스를 클러스터에서 운영하는 경우.

15. High Performance Computing (HPC)
설명: 대규모 연산을 필요로 하는 과학적 및 엔지니어링 작업을 지원하는 AWS 서비스입니다.
예시: 복잡한 시뮬레이션을 수행하는 연구 프로젝트.

16. AWS Snowcone device
설명: 작은 데이터 전송 및 엣지 컴퓨팅 장치로, 데이터를 AWS로 안전하게 전송합니다.
예시: 오프라인 환경에서 수집한 데이터를 클라우드로 전송하는 장치.

17. AWS Snowball Edge Storage Optimized device
설명: 대량의 데이터를 이동하거나 처리하는 데 사용되는 AWS 장치입니다.
예시: 원거리 위치에서 수집한 데이터를 S3로 전송하기 위해 사용하는 장치.

18. Popular Content Management System (CMS)
설명: 웹 콘텐츠를 관리하는 소프트웨어로, AWS에서 호스팅될 수 있습니다.
예시: WordPress를 사용하여 웹사이트 콘텐츠를 관리.

19. Amazon OpenSearch Service (Amazon Elasticsearch Service)
설명: 실시간 검색과 분석을 위한 분산 검색 엔진 서비스입니다.
예시: 로그 데이터 분석을 위한 Elasticsearch 클러스터 구성.

20. Kinesis Data Streams
설명: 실시간 데이터 스트리밍을 처리할 수 있는 서비스입니다.
예시: IoT 장치에서 수집한 데이터를 실시간으로 처리하고 분석.

21. AWS WAF
설명: 웹 애플리케이션 방화벽으로, 웹 애플리케이션을 악성 트래픽으로부터 보호합니다.
예시: 특정 IP 주소로부터의 요청을 차단하여 DDoS 공격 방어.

22. Associate Regional web ACLs
설명: 특정 리전의 리소스에 대한 웹 ACL(Access Control List)을 연결하는 기능입니다.
예시: 미국 동부 리전의 특정 CloudFront 배포에 웹 ACL을 연결.

23. AWS Firewall Manager
설명: 여러 계정 및 리전에서 AWS WAF 및 Shield를 중앙에서 관리할 수 있는 서비스입니다.
예시: 모든 AWS 계정에서 동일한 WAF 규칙을 일관되게 적용.

24. AWS Global Accelerator
설명: 사용자 요청을 최적의 AWS 리전으로 라우팅하여 성능을 개선하는 서비스입니다.
예시: 글로벌 사용자를 위해 최적의 리전으로 요청을 라우팅하여 빠른 응답 제공.

25. Origin Access ID (OAI)
설명: CloudFront에서 S3 버킷에 대한 액세스를 제어하기 위해 사용되는 식별자입니다.
예시: CloudFront가 S3 버킷에서 콘텐츠를 가져올 수 있도록 권한을 부여.

26. Disaster Recovery
설명: 재해 발생 시 데이터와 시스템을 복구하는 전략입니다.
예시: 주요 시스템의 백업을 정기적으로 수행하여 데이터 손실 방지.

27. AWS PrivateLink
설명: VPC에서 AWS 서비스에 안전하게 접근할 수 있도록 하는 기능입니다.
예시: VPC 내에서 S3에 안전하게 연결하는 경우.

28. AWS Database Migration Service (AWS DMS)
설명: 데이터베이스를 AWS로 또는 AWS 간에 쉽게 마이그레이션할 수 있는 서비스입니다.
예시: 온프레미스 Oracle 데이터베이스를 Amazon RDS로 이전.

29. AWS Schema Conversion Tool (AWS SCT)
설명: 데이터베이스 스키마를 다른 데이터베이스 엔진으로 변환하는 도구입니다.
예시: Oracle 스키마를 PostgreSQL 형식으로 변환.

30. Amazon MQ
설명: 관리형 메시지 브로커 서비스로, JMS 및 AMQP 프로토콜을 지원합니다.
예시: 기존의 메시징 시스템을 클라우드로 이전하여 운영.

31. RabbitMQ
설명: 오픈 소스 메시징 시스템으로, 다양한 프로그래밍 언어와 플랫폼을 지원합니다.
예시: 마이크로서비스 간의 비동기 통신을 위해 RabbitMQ를 사용하는 경우.

32. Amazon RDS for PostgreSQL
설명: PostgreSQL 데이터베이스를 클라우드에서 관리할 수 있도록 하는 서비스입니다.
예시: 웹 애플리케이션의 데이터베이스로 Amazon RDS for PostgreSQL 사용.

33. Compute Saving Plan
설명: AWS Compute 서비스에 대한 비용을 절감할 수 있도록 하는 요금제입니다.
예시: EC2 및 Fargate 사용량에 대한 할인 요금제를 구매.

34. Application Stack
설명: 특정 애플리케이션을 구축하는 데 필요한 모든 구성 요소의 집합입니다.
예시: 웹 서버, 데이터베이스, 캐시 서버로 구성된 애플리케이션 스택.

35. Amazon CloudWatch Synthetics
설명: 애플리케이션의 가용성을 모니터링하기 위해 자동화된 테스트를 수행하는 서비스입니다.
예시: 웹 애플리케이션의 URL을 정기적으로 확인하여 가용성을 모니터링.

36. AWS Control Tower
설명: AWS 환경을 설정하고 관리하는 데 도움을 주는 서비스입니다.
예시: 여러 AWS 계정을 중앙에서 관리하고 모범 사례를 적용하는 데 사용.

37. AWS Organizations
설명: 여러 AWS 계정을 중앙에서 관리할 수 있는 서비스입니다.
예시: 여러 부서의 AWS 계정을 단일 조직으로 통합 관리.

38. AWS Systems Manager Session Manager
설명: EC2 인스턴스에 대한 안전한 쉘 액세스를 제공하는 기능입니다.
예시: SSH 키 없이 인스턴스에 연결하여 관리 작업 수행.

39. Amazon Elastic Container Registry (Amazon ECR)
설명: Docker 컨테이너 이미지를 저장하고 관리할 수 있는 서비스입니다.
예시: CI/CD 파이프라인에서 애플리케이션 이미지를 ECR에 저장.

40. Amazon RDS Proxy
설명: RDS 데이터베이스에 대한 연결을 효율적으로 관리하는 프록시 서비스입니다.
예시: 애플리케이션의 데이터베이스 연결 수를 줄이고 성능을 개선.

41. DynamoDB
설명: 완전관리형 NoSQL 데이터베이스 서비스입니다.
예시: 사용자 정보를 저장하는 웹 애플리케이션의 데이터베이스.

42. Amazon DynamoDB Accelerator (DAX)
설명: DynamoDB의 인메모리 캐시 서비스로, 응답 속도를 개선합니다.
예시: 실시간 게임 데이터를 빠르게 조회하기 위해 DAX 사용.

43. AWS Systems Manager Parameter Store
설명: 애플리케이션 구성 데이터를 안전하게 저장하고 관리할 수 있는 서비스입니다.
예시: API 키와 같은 비밀 정보를 안전하게 저장하고 액세스.

44. AWS Shield Advanced
설명: AWS Shield Standard의 고급 버전으로, 추가적인 DDoS 보호 및 자동화된 응답 기능을 제공합니다.
예시: DDoS 공격에 대한 세부 보고서와 함께 실시간 보호.

45. AWS Shield Standard
설명: 기본 DDoS 방어 기능으로, 모든 AWS 고객에게 자동으로 제공됩니다.
예시: CloudFront와 같은 서비스에서 기본적으로 제공되는 DDoS 보호.

46. DynamoDB Streams
설명: DynamoDB 테이블의 변경 사항을 실시간으로 캡처하는 기능입니다.
예시: 데이터 변경 시 자동으로 알림을 보내는 애플리케이션.

47. DynamoDB Streams API
설명: DynamoDB Streams에서 스트림 데이터를 읽고 처리하는 API입니다.
예시: 변경 사항에 대해 트리거된 Lambda 함수로 데이터 처리.

48. Amazon DynamoDB
설명: 앞서 설명된 것과 동일한 완전관리형 NoSQL 데이터베이스 서비스입니다.

49. AWS Transfer Family
설명: SFTP, FTPS, FTP를 지원하는 관리형 파일 전송 서비스입니다.
예시: 안전한 파일 전송을 위해 S3와 연결된 SFTP 서버 구성.

50. S3 Object Lock in compliance mode
설명: S3 객체에 대한 삭제 방지를 보장하는 규정 준수 모드입니다.
예시: 법적 요구 사항을 충족하기 위해 데이터를 영구히 보존하는 경우.

51. S3 Object Lock in governance mode
설명: 객체를 보호하여 실수로 삭제되거나 변경되지 않도록 하는 모드입니다.
예시: 관리자가 특정 기간 동안 객체를 변경할 수 없도록 설정.

52. AWS Elastic Beanstalk
설명: 웹 애플리케이션을 손쉽게 배포하고 관리할 수 있는 플랫폼입니다.
예시: Node.js 애플리케이션을 Elastic Beanstalk에 배포하여 자동으로 인프라 관리.

53. Amazon Rekognition, Amazon Textract
설명: Rekognition은 이미지 및 비디오 분석 서비스, Textract는 문서에서 데이터를 추출하는 서비스입니다.
예시: Rekognition을 사용하여 얼굴 인식하고, Textract를 통해 스캔한 문서에서 텍스트를 추출.

54. Redis, Memcached
설명: 인메모리 데이터 구조 저장소로, 고속 데이터 엑세스를 위한 캐시 솔루션입니다.
예시: 웹 애플리케이션의 세션 데이터를 저장하기 위해 Redis를 사용.

55. AWS CloudFormation
설명: 인프라를 코드로 관리하고 자동으로 배포할 수 있는 서비스입니다.
예시: 인프라 설정을 YAML 파일로 정의하여 EC2와 RDS를 배포.

56. DynamoDB TTL
설명: DynamoDB 테이블에서 데이터 항목을 자동으로 만료시키는 기능입니다.
예시: 세션 데이터가 만료되도록 TTL 설정하여 자동으로 삭제.

57. Amazon Cognito
설명: 사용자 인증, 권한 부여 및 사용자 관리 서비스를 제공합니다.
예시: 모바일 애플리케이션에서 사용자가 안전하게 로그인할 수 있도록 하는 서비스.

1. Amazon Connect
설명: 클라우드 기반의 콜센터 서비스로, 고객과의 상호작용을 
관리할 수 있습니다.
예시: 고객 서비스 팀이 Amazon Connect를 사용하여 고객 전화 
응대 및 관리하는 시스템을 구축할 수 있습니다.

2. Amazon Pinpoint
설명: 사용자와의 커뮤니케이션을 위한 마케팅 캠페인을 
설계하고 실행할 수 있는 서비스입니다.
예시: 앱 사용자에게 SMS나 이메일을 통해 프로모션 메시지를 
보내는 데 사용됩니다.

3. Amazon Lake Formation
설명: 데이터 레이크를 쉽게 구축하고 관리할 수 있도록 돕는 
서비스입니다.
예시: 다양한 소스에서 데이터를 수집하여 중앙 집중식 데이터 
레이크를 만들고 분석할 수 있습니다.

4. Apache Parquet
설명: 열 기반의 저장 형식으로, 대규모 데이터 처리에 
최적화되어 있습니다.
예시: Amazon Athena에서 Parquet 파일을 사용하여 효율적으로 
쿼리할 수 있습니다.

5. AWS Management Console
설명: AWS 서비스를 관리할 수 있는 웹 기반 인터페이스입니다.
예시: EC2 인스턴스를 시작하거나 S3 버킷을 관리하는 데 
사용됩니다.

6. NAT Instance, NAT Gateway
설명: VPC의 프라이빗 서브넷에서 인터넷에 접근할 수 있도록 
하는 서비스입니다.
예시: 프라이빗 인스턴스가 소프트웨어 업데이트를 다운로드할 
때 NAT Gateway를 사용합니다.

7. AWS Systems Manager OpsItems
설명: 운영 문제를 중앙에서 관리하고 추적할 수 있는 
서비스입니다.
예시: 서비스 중단 문제를 기록하고 해결 상태를 추적하는 데 
사용됩니다.

8. Amazon CloudWatch Application Insights
설명: 애플리케이션의 상태를 모니터링하고 문제를 자동으로 
감지하는 서비스입니다.
예시: 웹 애플리케이션의 성능 저하를 감지하여 알림을 받을 수 
있습니다.

9. AWS Database Migration Service (AWS DMS)
설명: 데이터베이스를 AWS 클라우드로 또는 클라우드 간에 쉽게 
마이그레이션할 수 있는 서비스입니다.
예시: 온프레미스 데이터베이스를 Amazon RDS로 이전하는 데 
사용됩니다.

10. Peering
설명: 두 VPC 간의 네트워크 트래픽을 직접 연결할 수 있는 
기능입니다.
예시: 서로 다른 AWS 계정의 VPC 간에 리소스를 공유할 수 
있습니다.

11. Cost Explorer
설명: AWS 사용 비용을 분석하고 예측하는 데 도움을 주는 
도구입니다.
예시: 지난 6개월간의 AWS 비용을 시각적으로 분석하여 사용 
패턴을 이해합니다.

12. AWS Identity and Access Management (IAM)
설명: AWS 리소스에 대한 접근 권한을 관리할 수 있는 
서비스입니다.
예시: 특정 사용자에게 S3 버킷에 대한 읽기 권한만 부여할 수 
있습니다.

13. AWS Direct Connect
설명: 온프레미스 데이터 센터와 AWS 간의 전용 네트워크 연결을 
제공하는 서비스입니다.
예시: 대규모 데이터 전송 시 안정적인 연결을 위해 Direct 
Connect를 사용합니다.

14. DNS Routing Policy
설명: Route 53에서 DNS 요청을 처리하는 방법을 설정하는 
정책입니다.
예시: 가용성을 높이기 위해 여러 리전에서 서비스 요청을 
분산하는 데 사용됩니다.

15. AWS Storage Gateway
설명: 온프레미스 환경과 클라우드 스토리지 간의 하이브리드 
스토리지 서비스를 제공합니다.
예시: 기업이 기존 파일 시스템을 클라우드로 백업할 수 있도록 
도와줍니다.

16. VPC CIDR
설명: 가상 프라이빗 클라우드(VPC)의 IP 주소 범위를 정의하는 
방법입니다.
예시: VPC를 생성할 때 10.0.0.0/16과 같은 CIDR 블록을 
지정합니다.

17. Amazon CloudWatch Metric Stream
설명: CloudWatch 지표를 실시간으로 수집하고 전송하는 
기능입니다.
예시: 애플리케이션의 성능 지표를 외부 시스템으로 전송하여 
모니터링합니다.

18. Amazon Data Lifecycle Manager (Amazon DLM)
설명: EBS 볼륨의 스냅샷을 자동으로 생성하고 관리할 수 있는 
서비스입니다.
예시: 매일 스냅샷을 생성하고 보관 정책에 따라 삭제합니다.

19. Warm Standby Deployment
설명: 기본 인프라의 축소된 복제본을 유지하여 빠르게 복구할 
수 있도록 하는 전략입니다.
예시: 주요 데이터베이스의 리전 간 복제를 설정하여 재해 
복구를 준비합니다.

20. Pilot Light Deployment
설명: 핵심 시스템만을 최소한으로 유지하고 나머지는 필요할 때 
시작하는 복구 전략입니다.
예시: 재해 발생 시 애플리케이션의 기본 기능만 유지하고 
나머지는 비활성화합니다.

21. AWS CloudFormation
설명: 인프라를 코드로 관리하고 자동으로 배포할 수 있는 
서비스입니다.
예시: YAML 또는 JSON 파일을 사용해 EC2 인스턴스와 RDS를 
자동으로 배포합니다.

22. Amazon Macie
설명: 데이터 보호를 위한 머신 러닝 기반의 서비스로, S3에서 
민감한 정보를 식별하고 보호합니다.
예시: 고객의 개인 정보를 포함한 데이터를 찾아 자동으로 
알림을 보냅니다.

23. Amazon FSx for NetApp ONTAP
설명: 관리형 파일 스토리지 서비스로, NetApp의 기능을 
클라우드에서 제공합니다.
예시: 기업이 온프레미스 NetApp 파일 시스템을 AWS로 이전하여 
클라우드에서 사용하는 경우입니다.

24. Amazon Simple Email Service (Amazon SES)
설명: 이메일 전송 및 수신을 위한 클라우드 기반 서비스입니다.
예시: 마케팅 이메일이나 사용자 알림을 대량으로 발송하는 데 
사용됩니다.

25. Amazon Lightsail
설명: 간단한 애플리케이션과 웹사이트를 위해 설계된 가상 서버 
서비스입니다.
예시: 개인 블로그나 소규모 웹사이트를 운영하는 데 적합한 
서버를 쉽게 설정합니다.

26. Amazon WorkMail
설명: 클라우드 기반의 이메일 및 일정 관리 서비스입니다.
예시: 기업에서 전자 메일과 일정 관리를 위해 WorkMail을 
사용하는 경우입니다.

27. ASGAverageCPUUtilization
설명: Auto Scaling 그룹의 평균 CPU 사용률을 나타내는 
CloudWatch 지표입니다.
예시: CPU 사용률이 특정 임계값을 초과하면 Auto Scaling이 
추가 인스턴스를 생성하는 데 사용됩니다.