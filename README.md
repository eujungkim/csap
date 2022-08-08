# csap
## 주요 기능
### AWS SMS (AWS Server Migration Service)
https://docs.aws.amazon.com/ko_kr/server-migration-service/latest/userguide/server-migration.html
### AWS Batch
https://aws.amazon.com/ko/batch/
### AWS Budget
https://aws.amazon.com/aws-cost-management/aws-budgets/
### SCP (서비스 제어 정책)
https://docs.aws.amazon.com/ko_kr/organizations/latest/userguide/orgs_manage_policies_scps.html
### AWS PrivateLink
https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/aws-privatelink.html
### 배치 그룹
https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/placement-groups.html
### Linux에서 향상된 네트워킹 사용
https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/enhanced-networking.html
### AWS Shield Standard
https://aws.amazon.com/shield/
### Amazon RDS 스토리지 유형
https://docs.aws.amazon.com/ko_kr/AmazonRDS/latest/UserGuide/CHAP_Storage.html
## Exam Readiness
### Amazon EC2 Auto Scaling
- Scalable resources
- Manage cost
### Amazon ElastiCache
### Amazon SNS
- Amazon SNS pushed to subscribers
- Bulk notification
- Mobile push capability
### Amazon CloudFormation
### Elastic Load Balancing
- Two-way traffic
- Immediate request handling
### Amazon SQS
- Client poll Amazon SQS
- Persistent task storage
- Controlled completion mechanism
### Amazon Kinesis
- Scalable event streaming
- Clients read and track stream position
### Amazon CloudWatch
### AWS IAM
- IAM users and groups
### AWS STS
- Policies and roles
- AWS services interaction with the account
### AWS Lambda
- AWS service roles로 사용
### Amazon Cognito
- Identity providers
- 웹/모바일 앱에 대한 액세스 제어 및 인증을 제공하는 완전 관리형 솔루션
- MFA, SAML 지원
- social identity providers를 통한 로그인
- 사용자 이름과 암호를 사용하여 직접 로그인하거나 신뢰할 수 있는 서드 파티를 통해 로그인할 수 있음
- 미사용 데이터 및 전송 중 데이터 암호화
### AWS Directory Service
- SAML 2.0, single sign-on, OpenID Connect
- User Pools, Identity Pools


## 설명
- Lambda 함수는 15분 후에 제한 시간이 초과됩니다.
- VPC 흐름 로그를 생성합니다. 흐름 로그를 Amazon S3 버킷에 게시합니다. Amazon Athena에서 외부 테이블을 생성하여 로그 파일을 쿼리합니다. Amazon QuickSight에서 Amazon Athena에 연결하여 데이터를 시각화합니다.
- PrivateLink에서 제공하는 VPC 엔드포인스 서비스 활용 : 두 VPC의 클라이언트와 서버에 중복되는 IP 주소가 있는 경우 좋은 옵션이다. PrivateLink는 클라이언트 VPC 내에서 탄력적 네트워크 인터페이스를 사용하므로 서비스 공급자와 IP 주소 충돌이 발생하지 않는다. VPC 피어링, VPN 및 AWS Direct Connect 연결을 통해 PrivateLink 엔트포인트에 액세스할 수 있다.
- Elastic Network Adapter(ENA)를 통해 향상된 네트워킹이 활성화된 Amazon EC2 인스턴스 시작
- 클러스터 배치 그룹 : 대기시간 최소화
- 점보 프레임 : 네트워크 트래픽의 TCP/IP 오버헤드 감소
- DB 마이그레이션 가동 중시 시간 최소화 : Amazon RDS for MySQL DB, AWS Database Migration Service(AWS DMS), 전체 로드 및 변경 데이터 캡처(CDC) 마이그레이션 전략 사용
- VPN을 Direct Connect의 백업으로 사용
- AWS System Manager Parameter Store, AMS Key Management Service(kMS) CMK, ksm:Deceypt, ssm:GetParameter
- AMI는 특정 리전에서만 사용 가능. 다른 리전에서 사용하려면 AMI를 복사해야 함
- UpdateImte 호출이 증가된 개수를 저장할 떄 조건부 쓰기를 사용한다.
- MySQL > Amazon Aurota MySQL, Tomcat Java 애플리케이션 > Elastic Beanstalk
- Shield Standard : 애플리케이션 계층의 공격을 차단하지 않음. 계층 3과 4에서 동작
- 문자열 일치 조건을 사용하여 ALB에서 AWS WAF 규칙을 적용하여 잘뭇된 요청을 차단한다.
- Aurora는 최대 128TB의 데이터를 저장할 수 있음
- AWS Database Migration Service(AWS DMS)를 사용하여 데이터 마이그레이션
- 대용량 파일의 S3 업로드 성능 향상 방안 : S3 Transfer Acceleration 활성화, 비디오 파일을 청크로 분할하여 멀티파트 업로드를 사용해 S3로 파일 전송
- DB 인스턴스의 스토리지 유형을 프로비저닝된 IOPS SSD로 수정 : DB 인스턴스에서 처리할 수 있는 디스크 I/O의 양을 효과적으로 두 배로 향상
- AWS Managed Microsoft AD : AWS Cloud에서 managed Active Directory를 사용할 있게 함
- AD Connector : 온프레이스 사용자가 Active Directory를 통해 AWS 서비스를 사용할 수 있게 함
- Simple AD : low-scale, low-cost basic Active Directory capability 제공
- 동적 호스트 포트 매핑을 사용하면 컨테이너 인스턴스마다 동일 서비스의 여러 작업이 허용된다.
- 경로 기반 라우팅을 사용하면 여러 서비스가 단일 Application Load Balancer(ALB)에서 동일한 리스너 포트를 사용할 수 있다.
