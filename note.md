## Note
- **sts:AssumeRole** : 다른 계정의 권한을 일시적으로 얻도록 가정(assume)할 수 있음
- **aws-auth ConfigMap** : Kubernetes 클러스터 내에서 IAM 역할을 쿠버네티스 서비스 계정에 매핑
- **EC2 Image Builder** : 컨테이너 이미지 파이프라인을 자동화하는 데 사용
  - 이미지 빌드 프로세스 중에 취약성 검사를 자동으로 수행
- **AWS GuardDuty** : 네트워크 활동과 계정 활동에서 의심스러운 활동 및 잠재적인 보안 위협을 식별
  - 계정이나 서비스가 악용되는 것을 방지하고, 침입 시도, 데이터 유출, 기타 의심스러운 활동을 식별하는 데 사용 
  - **GuardDuty Malware Protection** : 주로 악성 소프트웨어 감지
- **AWS Inspector** : 애플리케이션의 보안 취약성과 규정 준수 상태를 자동으로 평가
- **AWS Config** : AWS 리소스와 관련된 구성 변경을 자동으로 추적하고 평가
