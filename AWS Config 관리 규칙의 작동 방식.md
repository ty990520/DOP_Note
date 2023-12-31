### AWS Config 관리 규칙의 작동 방식

1. **자동 평가:** AWS Config 관리 규칙은 주기적으로 또는 구성 변경이 발생할 때마다 자동으로 실행됩니다. 이는 리소스가 지정된 규칙을 준수하는지 여부를 평가합니다.

2. **적합성 판단:** 각 리소스는 규칙에 대해 '적합(Compliant)' 또는 '부적합(Non-compliant)'으로 평가됩니다. 예를 들어, S3 버킷의 퍼블릭 액세스 차단 규칙의 경우, 퍼블릭 액세스가 차단된 버킷은 '적합'으로, 차단되지 않은 버킷은 '부적합'으로 평가됩니다.

3. **알림 및 자동화:** 부적합한 구성이 감지되면 AWS Config는 이를 보고하며, 추가적인 조치를 위해 `Amazon SNS`, `AWS Systems Manager`, `Lambda 함수` 등과 통합할 수 있습니다.

4. **중앙 집중식 관리:** AWS Organizations와 통합되어, 여러 AWS 계정과 리전에 걸쳐 규칙을 적용하고 모니터링할 수 있습니다.

### 주 사용 사례

- **보안 및 규정 준수:** 특정 보안 기준과 규정 준수 요구 사항을 지키기 위한 리소스 구성을 모니터링하고 유지합니다.
- **변경 관리:** AWS 리소스의 구성 변경을 지속적으로 모니터링하고, 변경사항을 자동으로 감지하여 관리합니다.

AWS Config는 이처럼 AWS 환경의 구성 관리 및 감사에 매우 유용한 도구로, 리소스 구성의 변화와 규정 준수 상태를 지속적으로 모니터링하고 자동으로 평가합니다.
