## `sts:AssumeRole` vs `sts:AssumeRoleWithSAML`

| 특징             | sts:AssumeRole | sts:AssumeRoleWithSAML |
|----------------|----------------|------------------------|
| **정의**        | AWS 계정의 IAM 사용자나 서비스가 다른 계정의 IAM 역할을 임시로 가정할 수 있게 해주는 작업 | SAML(Security Assertion Markup Language) 2.0 기반의 연방 인증 정보를 사용하여 AWS 역할을 가정하는 작업 |
| **사용 사례**   | AWS 계정 간의 접근을 위해 사용. 예를 들어, 한 계정의 사용자가 다른 계정의 리소스에 접근 필요 | SAML 2.0을 지원하는 외부 ID 공급자(예: 회사의 싱글 사인온)를 통해 AWS에 인증할 때 사용 |
| **인증 방식**   | AWS IAM 자격 증명을 사용 | SAML 2.0 어설션(assertion)을 사용 |
| **적용 분야**   | AWS 서비스 또는 AWS 계정 간에 일반적으로 사용 | 기업의 싱글 사인온 구현과 같은 연방 로그인(federated login) 환경에서 주로 사용 |
| **보안 측면**   | AWS 자격 증명과 역할을 기반으로 보안 접근을 제공 | SAML 어설션을 기반으로 보안 접근을 제공하며, 외부 ID 공급자를 통한 인증을 가능하게 함 |
