## StatusCheckFailed_System vs StatusCheckFailed_Instance
AWS EC2 인스턴스의 CloudWatch 경보는 `StatusCheckFailed_System`과 `StatusCheckFailed_Instance` 두 가지 주요 상태 검사 지표를 사용합니다. 이들은 각각 다른 유형의 문제를 감지하며, 그에 따라 다른 조치가 취해질 수 있습니다.

### StatusCheckFailed_System

- **용도:** 이 지표는 AWS의 기본 인프라스트럭처 수준에서 발생하는 문제를 감지합니다. 이는 AWS가 관리하는 부분에 속하며, 일반적으로 사용자가 직접 해결할 수 없는 문제들입니다.
- **감지되는 문제:** 하드웨어 결함, 네트워크 연결 문제, 전원 관련 이슈 등 AWS 인프라와 관련된 문제입니다.
- **조치:** AWS에서 인스턴스를 자동으로 다른 하드웨어로 이동시켜 문제를 해결할 수 있습니다. 사용자는 이를 위해 CloudWatch 경보와 EC2 인스턴스 복구 기능을 설정할 수 있습니다.

### StatusCheckFailed_Instance

- **용도:** 이 지표는 EC2 인스턴스 자체 내에서 발생하는 문제를 감지합니다. 이는 사용자가 관리하고 해결할 수 있는 범위에 속합니다.
- **감지되는 문제:** 운영 체제의 문제, 인스턴스의 과부하, 잘못된 애플리케이션 구성 등 인스턴스 수준에서 발생하는 문제입니다.
- **조치:** 사용자는 이러한 문제를 해결하기 위해 인스턴스를 재부팅하거나 구성을 조정할 수 있습니다. CloudWatch 경보를 통해 이러한 문제가 감지되었을 때 자동으로 인스턴스를 재부팅하는 조치를 설정할 수 있습니다.

따라서, `StatusCheckFailed_System`은 AWS 인프라 관련 문제에 초점을 맞추고, `StatusCheckFailed_Instance`는 사용자 수준에서 관리되는 인스턴스 관련 문제에 대응하는 데 사용됩니다.
