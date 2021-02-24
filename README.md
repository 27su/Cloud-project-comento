
**고객사 시스템 구축**
1. AWS 클라우드 환경 구성을 구축합니다.
2. 쿠버네티스 기반의 EKS 환경 구성과 웹 서비스 구축합니다.

**고객사 시스템 운영**
1. EKS 환경에서 로그 수집을 위한 EFK Stack을 구축합니다.
2. 백업 및 복구 정책, 보안 정책, 모니터링, 타사 솔루션 검토를 진행합니다

![image](https://user-images.githubusercontent.com/32132152/108957408-c074c100-76b4-11eb-8b3c-bec082ec80c9.png)

**1주차**

![image](https://user-images.githubusercontent.com/32132152/108957838-81933b00-76b5-11eb-825a-bd2c49367f22.png)

![image](https://user-images.githubusercontent.com/32132152/108958080-ccad4e00-76b5-11eb-8fda-e5e319f877b9.png)

![image](https://user-images.githubusercontent.com/32132152/108958142-e484d200-76b5-11eb-826c-b4a1a80a5ad7.png)

1. AWS IAM User 생성과 MFA 설정
- IAM 계정 설정
- MFA 설정 

2. VPC 구축과 NAT 인스턴스 생성
- NAT instance용 키 페어 생성 
- VPC 
- Subnet
- Internet Gateway
- Route Table

3. Bastion Host
- 보안그룹 설정
- Putty 접속
- os 계정 생성과 sudo 권한 부여
- 비밀번호 로그인 허용



**2주차**

: 쿠버네티스 기반의 EKS 환경 구성과 웹 서비스 구축

![image](https://user-images.githubusercontent.com/32132152/108958753-c2d81a80-76b6-11eb-84bb-eb90e25ea418.png)

![image](https://user-images.githubusercontent.com/32132152/108958830-e0a57f80-76b6-11eb-9f5e-5ad6c36ca49b.png)

![image](https://user-images.githubusercontent.com/32132152/108958858-ed29d800-76b6-11eb-9b0e-6e0ebfae0fd2.png)

1. Kubernetes
- 쿠버네티스란
- 쿠버네티스 클러스터 아키텍처
- 쿠버네티스 오브젝트

2. EKS 환경구성 - eksctl 명령어 사용
- Bastion에 kubectl 설치 (리눅스)
- EKS 클러스터와 NodeGroup 생성

3. Niginx 서비스 배포
- Nginx deployment 배포
- Nginx service 배포

4. Cluster와 NodeGroup 삭제



**3주차**

: EFK Stack 구축을 통한 로그 수집

1. 컨테이너 환경에서의 로그수집을 위해 EFK(Elastic search + Fluentd + Kibana) Stack을 구축
2. 로그 저장소인 Elastic Search, 로그 수집기인 Fluentd, 로그 시각화 툴인 Kibana를 EKS 환경에서 구축

1) Elastic Search 구축
2) Fluentd 구축
3) Kibana 구축

- EFK Stack
- Elastic Search
- Kibana
- Fluentd
- Kibana로 로그 시각화

![image](https://user-images.githubusercontent.com/32132152/108959743-2dd62100-76b8-11eb-87f8-6cc2e92f3abd.png)

*Elastic Search 배포 후 pod, service, web 화면

![image](https://user-images.githubusercontent.com/32132152/108959833-54945780-76b8-11eb-94e6-e90d76f6a5f3.png)

*Kibana 배포 후 pod, service, web 화면

![image](https://user-images.githubusercontent.com/32132152/108959883-683fbe00-76b8-11eb-87e6-5b84343f8a39.png)

![image](https://user-images.githubusercontent.com/32132152/108959903-71308f80-76b8-11eb-8ba7-9453b0de04a2.png)

*fluentd 배포 후 pod 화면

![image](https://user-images.githubusercontent.com/32132152/108959943-7db4e800-76b8-11eb-9d28-f256206bd5b9.png)

*Kibana에서 로그 수집하여 시각화한 화면

![image](https://user-images.githubusercontent.com/32132152/108959981-8c9b9a80-76b8-11eb-9394-d327477645c9.png)



**4주차**

AWS 시스템 운영
: 운영하면서 고려할 사항, 백업 및 복구 정책, 모니터링 요소와 서비스 활용, 타사 솔루션 검토

1. 모니터링 체크리스트 작성
2. 백업 및 복구 정책 (EC2 - lifeCyleManager(volume backup), AMI 등)
3. AWS Native 서비스를 이용한 모니터링 (CloudWatch Dashboard 구성, CloudTrail, Config, VPC Flowlogs 등)
4. 클라우드 모니터링 솔루션 제안 (Whatap kube(사용서비스), Grafana + Prometheus 자체 구축, data dog 등)



**5주차**

1. 운영이란 ?
2. 휴먼 에러 사례
3. AWS 운영 팁
