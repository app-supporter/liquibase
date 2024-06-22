<div align="center">
  
![image](https://avatars.githubusercontent.com/u/170791409?s=400&u=dc5c8ff1ff0be4e08bd47e773f94db276f48896d&v=4)

</div>
  
<div align="center">
  
  
  [📚 스터디 모집, 학습 공유 플랫폼](https://lnshare-study.com/) <br>

  [![Release](https://img.shields.io/badge/-📚_API_Documentation-green)](https://lnshare-study.com/) [![Release](https://img.shields.io/badge/-📚_Team_Blog-blue)]() [![Release](https://img.shields.io/badge/-📚_PR-blue)]() <br/>
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()

</div>
<br/>

<br/><br/><br/><br/>

<div align="center">
  
  ### **📚 Table of contents.** 

</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[1. 서비스 소개]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[2. 사용된 기술]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[3. Infrastructure]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[4. CICD<br/>]()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[5. 모듈 연관관계<br/>]()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[6. 패키지 구조<br/>]()

<br/><br/><br/><br/><br/><br/><br/>

# 👋 서비스 소개.

<br/><br/><br/><br/><br/><br/><br/>

# ✨ 사용된 기술.

Backend, Infrastructure, 협업에 사용된 기술 스택/툴은 다음과 같습니다.

<br/>

## 🖥️ Backend.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FG9Nmi%2FbtsH9FZOYqq%2FmoUcUwmJZ4Mz9Lxz4LVKc1%2Fimg.png)

> 공개되는 API 문서는 RestDocs를, 개발 서버에는 Swagger + RestDocs를 조합해 사용하고 있습니다. 개발 서버 API 문서는 조회할 수는 있지만 AWS Inbound 룰로 인해 사용할 수는 없습니다.  

<br/><br/><br/><br/><br/><br/>

## ☁️ InfraStructure.

서비스 구축을 위해 AWS를 활용했으며, 정적 자원은 S3와 CloudFront를, 서버 오케스트레이션은 AWS ECS를 사용했습니다. 각 리소스는 VPC 내부 별도의 서브넷(Public/Private)에 존재하며, ALB, NAT를 통해 외부와 통신합니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FMJrxl%2FbtsH8D9VGQD%2F3iBRoE6uo58NXsl9e2r260%2Fimg.png)

<br/><br/><br/><br/>

운영 로그와 시스템 로그를 별도로 관리하고 있으며, 운영 로그는 Grafana Loki를, 시스템 로그는 AWS CloudWatch로 관리하고 있습니다. 인프라 코드와 더 자세한 설명은 [해당 레포지토리]()를 참조해주세요.

![image]()

<br/><br/><br/><br/><br/><br/>

## 👬 Collaboration.

협업 툴은 이슈 트래킹을 위해 Jira/Confluencer를, 자동화 툴은 ZAPIer와 GitAction을 사용했습니다. 팀원 간 커뮤니케이션은 Slack으로 이루어지며, 또한 이를 통해 CICD 과정에서 발생한 리포트, AWS 비용 결과를 보고 받고 있습니다. 팀원 간 코드 컨벤션 관리 및 코드 스멜 제거를 위해 CheckStlye, PMD, SpotBugs, Sonarqube와 같은 정적 코드 분석 툴을 도입했습니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FofFbV%2FbtsH9GLbQKK%2FyJNQ4fKw2DK1VaW6vRbpY1%2Fimg.png)

> 팀 규칙 및 기술 관련 글은 [Gitbook]()을 사용해 관리하고 있습니다.

<br/><br/><br/><br/><br/><br/><br/>

# 🐋 CICD.

PR이 생성되면 자동으로 정적 분석을 시작하며, Slack으로 결과를 보고받습니다. 팀원 간 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 개발 서버로 배포가 되며, 인수 테스트가 시작됩니다. 자동 인수 테스트 외에도 QA를 진행하며 기능의 동작 유무, 버그 리포팅을 합니다. main 브랜치로 병합이 되면 상용 서버로 배포가 되며, 최종 결과를 보고받습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

<br/><br/><br/><br/><br/><br/><br/>

# 👨‍👩‍👦 모듈 연관관계

프로젝트에 사용된 모듈은 **`dailyge-API`**, **`admin-API`**, **`storage`**, **`support`** 모듈 입니다. 각 모듈의 기능은 다음과 같습니다. 

1. **`dailyge-API`**: 서비스 API 모듈입니다.
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

모듈간 의존관계는 다음과 같습니다. 불필요한 의존성 제거, 빌드 시간 단축을 위해 위해 Spring Data Jpa를 제외하고는 runtimeOnly 또는 imeimplementation [구성(Configuration)](https://docs.gradle.org/current/userguide/declaring_dependencies.html)을 사용하고 있습니다.

<br/>

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcHD02o%2FbtsH8G6bEze%2FgkOXvPS5h9ZNeIdKRDl9VK%2Fimg.png)

<br/><br/><br/><br/>

Spring Data Jpa는 imeimplementation을 사용하면 (캡슐화로 인해) 다른 모듈에서 import 할 수 없기 때문에 API를 사용하고 있습니다. 이는 도메인 모델과 영속 모델을 분리할 경우, imeimplementation을 사용할 수 있지만, 도메인 모델로 인해 늘어나는 코드량, 이로 인한 유지보수 비용이 더 크다고 판단해 도입하지 않았습니다.

```java
dependencies {
    // JPA
    API("org.springframework.boot:spring-boot-starter-data-jpa")

    ......
}
```

<br/><br/><br/><br/><br/><br/><br/>

# 📁 패키지 구조

core 패키지는 , common 패키지는 프로젝트에서 공통으로 사용되는 . 상위 모듈은 하위 모듈에 의존하지 않으며, 잘 변하지 않는 

```shell
.
├── dailyge-API
│     ......
│       └─ app
│           ├─ common    # 프로젝트 공통 패키지
│           └─ core      # 서비스 API 패키지
│               └─ user     # 도메인            
│                   ├─ external         #  외부 시스템 호출 계층       - Optional
│                   ├─ presentation     #  표면 계층(Controller)            
│                   ├─ facade           #  퍼사드 계층(Facade)       - Optional
│                   ├─ application      #  서비스 계층(Service)               
│                   └─ persistence      #  영속 계층(Repository)            
└── 

......

```

<br/><br/><br/><br/><br/><br/>

패키지 순환 참조가 발생하지 않도록 주기적으로 패키지 사이클을 관리하고 있습니다. 

![image]()

<br/><br/><br/><br/><br/><br/><br/>

# Contributors

| [Youl](https://github.com/kkk5474096) | [Jun](https://github.com/unam98) | []()| []()|
| :---: | :---: | :---: |:---: |
|<img width="100" src="https://github.com/depromeet/TeumTeum-Android/assets/89737271/513cb651-bc4a-4b91-85f3-5090da6cfc4a.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">| 
|**Backend, UI**|**Backend, Infra**| | |


<br/><br/><br/><br/><br/><br/><br/>


