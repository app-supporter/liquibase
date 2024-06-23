<div align="center">
  
  <img width="400" src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FVbllW%2FbtsH955a4cs%2FFNf8S3KK7u2h7L1GtJRKKk%2Fimg.png"><br/>
</div>
  
<div align="center">
  
  
  [📚 스터디 모집, 학습 공유 플랫폼](https://lnshare-study.com/) <br>

  [![Release](https://img.shields.io/badge/-📚_API_Docs-brightgreen)]() [![Release](https://img.shields.io/badge/-📚_Team_Blog-blue)]() <br/>
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()

</div>

<br/><br/>

<div align="center">
  
  ### **📚 Table of contents.** 

</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[1. 서비스 소개](https://github.com/Labs-Supporter/liquibase?tab=readme-ov-file#1-%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%86%8C%EA%B0%9C)<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[2. 사용된 기술](https://github.com/Labs-Supporter/liquibase?tab=readme-ov-file#2%EC%82%AC%EC%9A%A9%EB%90%9C-%EA%B8%B0%EC%88%A0)<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[3. CICD<br/>]()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[4. Architecture]()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[5. 모듈 연관관계<br/>]()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[6. 패키지 구조<br/>]()

<br/><br/><br/><br/>

# 1. Service Introduction.

<br/><br/><br/><br/><br/><br/><br/>

# 2. Skills.

Backend, Infra, 협업에 사용된 기술 스택/툴은 다음과 같습니다.

1. [Backend]()

2. [Infra]()

3. [Collaboration]()

<br/><br/><br/>

## 🖥️ Backend.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FG9Nmi%2FbtsH9FZOYqq%2FmoUcUwmJZ4Mz9Lxz4LVKc1%2Fimg.png)

> 공개 API 문서는 RestDocs를, 개발 서버에는 Swagger + RestDocs를 조합해 사용하고 있습니다. 외부인의 경우, [개발 서버 API 문서]()를 조회할 수는 있지만 AWS Inbound 룰로 인해 사용할 수는 없습니다.  

<br/><br/><br/><br/><br/><br/>

## ☁️ Infra.

서비스 구축을 위해 AWS를 활용했으며, 모니터링은 Prometheus와 Grafana를 사용하고 있습니다. 운영 로그는 Grafana Loki를, 시스템 로그는 AWS CloudWatch로 관리하고 있으며, 운영 과정에서 발생하는 이슈는 AWS Lambda로 보고받고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbcU6So%2FbtsH8Nkm8aQ%2FEneyp26AkfimW78whEvwmK%2Fimg.png)

> 비용 절감을 위해 일부 서버는 Google Cloud 무료 서비스를 활용하고 있습니다. 

<br/><br/><br/><br/><br/><br/>

## 👬 Collaboration.

협업 툴은 이슈 트래킹을 위해 Jira/Confluencer를, 자동화 툴은 Zapier와 GitAction을 사용하고 있습니다. 팀원 간 커뮤니케이션은 Slack으로 이루어지며, 또한 CICD 과정에서 발생한 리포트, AWS 비용 결과도 Slack을 통해 보고 받고 있습니다. 팀원 간 코드 컨벤션 관리 및 코드 스멜 제거를 위해 CheckStlye, PMD, SpotBugs, Sonarqube, Codev와 같은 정적 코드 분석 툴을 도입했습니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FS4C8q%2FbtsIaFkRVfB%2FLL4VJpYGVJZLMKi6h5yed1%2Fimg.png)

> 팀 규칙 및 기술 관련 글은 문서 관리의 용이성을 위해 [Gitbook]()을 사용하고 있습니다.

<br/><br/><br/><br/><br/><br/><br/>

# 3. CICD

PR이 생성되면 자동으로 정적 분석을 시작하며, Slack으로 결과를 보고받습니다. 팀원 간 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 개발 서버로 배포가 되며, 인수 테스트가 시작됩니다. 자동 인수 테스트 외에도 QA를 진행하며 기능의 동작 유무, 버그 리포팅을 합니다. main 브랜치로 병합이 되면 상용 서버로 배포가 되며, 최종 결과를 보고받습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

테스트 코드를 작성하지 않거나 테스트가 실패하는 경우, 또는 테스트 커버리지를 충족하지 못하면 빌드가 실패하게 됩니다. 테스트를 통과하더라도 코드 레벨에서는 발견하지 못하는 이슈를 찾기 위해 개발서버에서 QA를 진행합니다. 

![image]()

<br/><br/><br/><br/><br/><br/>

# 4. Architecture

정적 자원은 S3와 CloudFront를, 서버 오케스트레이션은 AWS ECS를 사용했습니다. 각 리소스는 VPC 내부 별도의 서브넷(Public/Private)에 존재하며, ALB와 NAT를 통해 외부와 통신합니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FMJrxl%2FbtsH8D9VGQD%2F3iBRoE6uo58NXsl9e2r260%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 5. Module

프로젝트에 사용된 모듈은 **`dailyge-API`**, **`admin-API`**, **`storage`**, **`support`** 모듈 입니다. 각 모듈의 기능은 다음과 같습니다. 

1. **`dailyge-API`**: 서비스 API 모듈로 입니다.
2. **`scheduler`**: 스케줄링 모듈입니다.
3. **`storage`**: 데이터베이스 모듈입니다.
4. **`support`**: 로깅, 모니터링 등 API 모듈을 지원하는 모듈입니다.

<br/><br/><br/><br/>

도메인 모델과 영속 모델은 별도로 구분하지 않았으며, 영속 모델을 도메인 모델로 사용하고 있습니다. 

```shell
├── storage
│    ......
│       └─ dailyge
│             └─ entity  # 영속 모델

```

<br/><br/><br/><br/>

모듈간 의존관계는 다음과 같습니다. 불필요한 의존성 제거, 빌드 시간 단축을 위해 위해 대체로 runtimeOnly 또는 imeimplementation [구성(Configuration)](https://docs.gradle.org/current/userguide/declaring_dependencies.html)을 사용하고 있습니다.

<br/>

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcHD02o%2FbtsH8G6bEze%2FgkOXvPS5h9ZNeIdKRDl9VK%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 6. Package

core 패키지는 서비스에 관한 기능을, common 패키지는 프로젝트에서 공통으로 사용되는 클래스 또는 설정을 포함하고 있습니다. 상위 계층은 하위 계층에 의존하지 않으며, 하위 계층의 존재를 알지 못합니다.

```shell
.
├─📁 dailyge-API
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

> 각 계층의 의존도는 다음과 같습니다. 숫자가 작을수록 하위 계층입니다. <br/>
> Controller(1)  -->  Facade(2)  -->  Application(3), External(3)  -->  Persistence(4)

<br/><br/><br/><br/><br/><br/>

패키지 순환 참조가 발생하지 않도록 주기적으로 패키지 사이클을 관리하고 있습니다. 

![image]()

<br/><br/><br/><br/><br/><br/><br/>

https://blog.kakaocdn.net/dn/bnh60B/btsH9fOa0cF/fBhedhfckO4gyijcSMGuAk/img.png

# Contributors

| [Youl](https://github.com/kkk5474096) | [Jun](https://github.com/unam98) |
| :---: | :---: |
|<img width="150" src="https://github.com/depromeet/TeumTeum-Android/assets/89737271/513cb651-bc4a-4b91-85f3-5090da6cfc4a.jpg">|<img width="150" src="https://avatars.githubusercontent.com/u/92818747?v=4">|
|**Backend, Frontend**|**Backend, Infra**|


<br/><br/><br/><br/><br/><br/><br/>


