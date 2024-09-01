<br/><br/>

<div align="center">
  <img width="400" src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FCl3Zr%2FbtsH9tFrQxe%2F4Wd1nL8FuHANpzi9flDwBK%2Fimg.png"><br/><br/>
</div>

<div align="center">

Dailyge로 일정 관리를 간편하게! <br>
성실한 하루의 연속이 큰 변화를 가져옵니다. 🏃

[![Release](https://img.shields.io/badge/-📆_Web_Service-blue)](https://www.dailyge.com/) [![Release](https://img.shields.io/badge/-📚_API_Docs-brightgreen)]() <br/>
[![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v0.0.0-brightgreen)](https://www.dailyge.com/)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=dailyge_dailyge-server&metric=coverage)](https://sonarcloud.io/summary/new_code?id=dailyge_dailyge-server)

</div>

<br/><br/><br/><br/><br/><br/>

# 1. Table of Contents.

1. 서비스 소개
2. Skills
3. CICD
4. Architecture
5. Moduels
6. Package


<br/><br/><br/><br/><br/><br/><br/>

# 1. Service Introduction.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbGAESd%2FbtsJnrmbCzr%2FI3OIR1VM5LFYxuMnXrP9X1%2Fimg.png)

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FEVA0Y%2FbtsJnhxeyvw%2FxEpotIGhrNVG8Gb9VWlPxk%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 2. Skills.

Backend, Infra, 협업에 사용된 기술 스택/툴은 다음과 같습니다.

1. [Backend]()

2. [Infra]()

3. [Collaboration]()

<br/><br/><br/>

## 🖥️ Backend.

Java/SpringBoot를 사용해 애플리케이션을 구축했습니다. Liquibase로 데이터베이스 스키마를 추적하고 있으며, 공개 API 문서는 RestDocs를, 개발 서버에는 Swagger + RestDocs를 조합해 사용하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FG9Nmi%2FbtsH9FZOYqq%2FmoUcUwmJZ4Mz9Lxz4LVKc1%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

## ☁️ Infra.

서비스 구축을 위해 AWS를 활용했으며, 모니터링은 Prometheus와 Grafana를 사용하고 있습니다. 운영 로그는 Grafana Loki, 시스템 로그는 AWS CloudWatch로 관리하고 있으며, 운영 과정에서 발생하는 이슈는 AWS Lambda로 보고받고 있습니다. 비용 절감을 위해 일부 서버는 Google Cloud를 활용하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FRUR1K%2FbtsJebYQ9S7%2Fpr8dSua2YHDtpnNlQ6bdR1%2Fimg.png)

> 인프라에 대한 상세한 내용은 [해당 링크](https://github.com/dailyge/dailyge-infra)를 참조해주세요.

<br/><br/><br/><br/><br/><br/>

## 👬 Collaboration.

협업 툴은 이슈 트래킹을 위해 Jira/Confluencer를, 자동화 툴은 Zapier와 GitAction을 사용하고 있습니다. 팀원 간 커뮤니케이션은 Slack으로 이루어지며, 또한 CICD 과정에서 발생한 리포트, AWS 비용 결과도 Slack으로 보고 받고 있습니다. 팀원 간 코드 컨벤션 관리 및 코드 스멜 제거를 위해 CheckStlye, PMD, SonarCloud와 같은 정적 코드 분석 툴을 사용하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fl2pkf%2FbtsJd9tyhbM%2FvEkghskriwATuz7kFAl5x0%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 3. CICD

PR이 생성되면 자동으로 정적 분석을 시작하며, Slack으로 결과를 보고받습니다. 팀원 간 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 개발 서버로 배포가 되며, 인수 테스트가 시작됩니다. 자동 인수 테스트 외에도 QA를 진행하며 기능의 동작 유무, 버그 리포팅을 합니다. main 브랜치로 병합이 되면 상용 서버로 배포가 되며, 최종 결과를 보고받습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

> 테스트 코드를 작성하지 않거나 테스트가 실패하는 경우, 또는 테스트 커버리지를 충족하지 못하면 빌드가 실패하게 됩니다. 개발서버에서 QA를 진행해 코드 레벨에서 발견할 수 없는 버그를 한 번 더 검증합니다. 

<br/><br/><br/><br/><br/><br/>

# 4. Architecture

정적 자원은 S3와 CloudFront를, 서버 오케스트레이션은 AWS ECS를 사용했습니다. 각 리소스는 VPC 내부 별도의 서브넷(Public/Private)에 존재하며, ALB와 NAT를 통해 외부와 통신합니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FRUR1K%2FbtsJebYQ9S7%2Fpr8dSua2YHDtpnNlQ6bdR1%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 5. Module

프로젝트에 사용된 모듈은 **`admin-api`**, **`dailyge-api`**, **`storage`**, **`support`** 모듈 입니다. 각 모듈의 기능은 다음과 같습니다. 

1. admin-api: 관리자 API 모듈로 입니다.
2. dailyge-api: 서비스 API 모듈로 입니다.
4. storage: 데이터베이스 모듈입니다.
5. support 로깅, 모니터링 등 API 모듈을 지원하는 모듈입니다.

<br/><br/><br/><br/>

도메인 모델과 영속 모델은 별도로 구분하지 않았으며, 영속 모델을 도메인 모델로 사용하고 있습니다. 도메인 모델로 인해 늘어나는 코드량, 이로 인한 유지보수 비용이 더 크다고 판단했기 때문입니다.

```shell
├─ 📁storage
│    ......
│       └📁 dailyge
│             └📁 entity   # 영속 모델

```

<br/><br/><br/><br/>

모듈간 의존관계는 다음과 같습니다. 불필요한 의존성 제거, 빌드 시간 단축을 위해 위해 대체로 runtimeOnly 또는 imeimplementation [구성(Configuration)](https://docs.gradle.org/current/userguide/declaring_dependencies.html)을 사용하고 있습니다.

<br/>

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcHD02o%2FbtsH8G6bEze%2FgkOXvPS5h9ZNeIdKRDl9VK%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 6. Package

core 패키지는 서비스에 관한 기능을, common 패키지는 프로젝트에서 공통으로 사용되는 클래스 또는 설정을 포함하고 있습니다. 상위 계층은 하위 계층에 의존하지 않으며, 하위 계층의 존재를 알지 못합니다.

```shell
├─📁 dailyge-api
│     ......
│       └─📁 app
│           ├─📁 common                       # 프로젝트 공통 패키지
│           └─📁 core       
│             └─📁 user                       # 도메인
│                ├─📁 external                # 외부 시스템 호출 계층         - Optional
│                ├─📁 presentation            # 표면 계층  
│                ├─📁 facade                  # 퍼사드 계층                 - Optional
│                ├─📁 application             # 서비스 계층
│                └─📁 persistence             # 영속 계층
└── 

......

```

```text
각 계층의 의존성은 다음과 같습니다.
> Controller  -->  Facade  -->  Application, External  -->  Persistence
```

<br/><br/><br/><br/><br/><br/>

패키지 순환 참조를 막기 위해 주기적으로 패키지 사이클을 관리하고 있습니다. 

![image]()

<br/><br/><br/><br/><br/><br/><br/>

# Contributors

<div align="center">

| [Youl](https://github.com/beatmeJY) | [Jun](https://github.com/devjun10) | [Yui](https://github.com/kmularise) |
| :---: | :---: | :---: |
|<img width="150" src="https://avatars.githubusercontent.com/u/54700818?v=4">|<img width="150" src="https://avatars.githubusercontent.com/u/92818747?v=4">|<img width="150" src="https://avatars.githubusercontent.com/u/106499310?v=4">|
|**Backend, Frontend**|**Backend, Infra**|**Backend**|

</div>
