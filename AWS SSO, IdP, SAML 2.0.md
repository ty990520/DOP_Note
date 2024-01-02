## `AWS SSO`, `IdP`, `SAML 2.0`
AWS IAM Identity Center(이전에는 AWS Single Sign-On 또는 AWS SSO로 알려짐)와 외부 자격 증명 공급자(IdP), SAML 2.0에 대해 쉽게 설명해드리겠습니다.

### AWS IAM Identity Center (AWS SSO)

- **정의:** AWS IAM Identity Center는 AWS 계정 및 비즈니스 애플리케이션에 대한 단일 로그인 접근을 제공하는 서비스입니다. 사용자는 하나의 중앙 집중식 사용자 인터페이스를 통해 여러 AWS 계정 및 애플리케이션에 액세스할 수 있습니다.

### 외부 자격 증명 공급자 (IdP)

- **정의:** IdP(Identity Provider)는 사용자의 신원 정보를 관리하고 인증하는 시스템입니다. 예를 들어, Okta, Microsoft Active Directory와 같은 서비스가 여기에 해당합니다.
- **역할:** IdP는 사용자의 로그인 정보(예: 사용자 이름, 비밀번호)를 관리하고, 해당 사용자가 누구인지 확인하는 역할을 합니다.

### SAML 2.0

- **정의:** SAML(Security Assertion Markup Language) 2.0은 웹 기반 인증 및 권한 부여를 위한 XML 기반의 오픈 표준입니다. 
- **용도:** SAML을 사용하면 사용자는 한 시스템(IdP)에서 인증을 받고 다른 시스템(AWS)에서 이를 인식하여 액세스를 허용할 수 있습니다. 이는 "싱글 사인온" 또는 SSO를 가능하게 합니다.

### 프로세스

1. **AWS IAM Identity Center 구성:** DevOps 팀은 AWS IAM Identity Center를 설정하여 조직 내 모든 사용자가 AWS 리소스에 액세스할 수 있도록 합니다.

2. **IdP와 연동:** 팀은 외부 IdP와 AWS IAM Identity Center를 연결합니다. 이를 통해 사용자는 자신이 이미 사용하는 IdP(예: 회사 이메일)로 AWS에 로그인할 수 있습니다.

3. **SAML 2.0 설정:** SAML 2.0을 사용하여 IdP와 AWS IAM Identity Center 간의 인증 및 권한 부여 절차를 설정합니다. 이렇게 하면 사용자가 IdP를 통해 인증하면 AWS IAM Identity Center가 이를 인식하고 AWS 리소스에 대한 액세스를 허용합니다.

4. **권한 관리:** DevOps 팀은 각 사용자 또는 그룹에 대한 권한을 설정하여, 특정 AWS 리소스에 대한 액세스를 관리합니다. 이 과정에서 최소 권한 원칙을 적용하여, 사용자가 필요한 리소스에만 접근할 수 있도록 합니다.

이러한 접근 방식을 통해, DevOps 팀은 AWS 리소스에 대한 보안 및 효율적인 액세스 관리를 수행할 수 있습니다.
