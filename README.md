
<div align="center">

![image](https://avatars.githubusercontent.com/u/170791409?s=400&u=dc5c8ff1ff0be4e08bd47e773f94db276f48896d&v=4)

</div>
  
<div align="center">
  
  
  [📚 스터디 모집, 학습 공유 플랫폼](https://lnshare-study.com/) <br>

  [![Release](https://img.shields.io/badge/-%F0%9F%92%AB%20Web%20Service-blue)](https://lnshare-study.com/)
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]() [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]() <br/>
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()

</div>
<br/>

<br/><br/><br/><br/>

<div align="center">
  
  ### **📚 Table of contents.** 

</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[1. 서비스 소개]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[2. 사용된 기술]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[3. Infrastructure]()<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[4. CICD<br/>]()

<br/>


# ✨ Backend.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FG9Nmi%2FbtsH9FZOYqq%2FmoUcUwmJZ4Mz9Lxz4LVKc1%2Fimg.png)

<br/><br/><br/>

# ☁️ InfraStructure.

서비스 구축을 위해 AWS를 활용했으며, 서버 오케스트레이션을 관리하기 위해 AWS ECS를 사용했습니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FMJrxl%2FbtsH8D9VGQD%2F3iBRoE6uo58NXsl9e2r260%2Fimg.png)

<br/><br/><br/>

운영 로그와 시스템 로그를 별도로 관리하기 위해 

<br/><br/><br/><br/><br/><br/><br/>

# 🐳 CICD.

PR이 생성되면 코드 **`정적 분석`** 을 합니다. 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 dev 서버에 배포가 되며, QA과정을 거친 후, prod 서버로 배포가 이루어 집니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

<br/><br/><br/><br/><br/>

협업/자동화 툴은 이슈를 트래킹하기 위해 Jira/Confluencer를 사용했으며, Slack을 통해 결과를 받고 있습니다. 팀원 간 코드 컨벤션 관리 및 코드 스멜 제거를 위해 CheckStlye, PMD, SpotBugs, Sonarqube와 같은 정적 코드 분석 툴을 도입했습니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FofFbV%2FbtsH9GLbQKK%2FyJNQ4fKw2DK1VaW6vRbpY1%2Fimg.png)

> 팀 규칙 및 기술 관련 글은 한 곳에서 관리하기 위해 [Gitbook]()을 사용했습니다.

<br/><br/><br/><br/><br/><br/><br/>

# 👨‍👩‍👦 모듈 연관관계

프로젝트에 사용된 모듈은 **`dailyge-api`**, **`admin-api`**, **`storage`**, **`support`** 모듈 입니다. 도메인 모델과 영속 모델은 별도로 구분하지 않았습니다.

1. **`dailyge-api`**: 서비스 API 모듈입니다.
2. **`scheduler`**: 스케줄링 모듈입니다.
3. **`storage`**: 데이터베이스 모듈입니다.
4. **`support`**: 로깅, 모니터링 등 API 모듈을 지원하는 모듈입니다.

<br/><br/><br/><br/>

모듈간 연관관계는 다음과 같습니다. 모듈에 대한 설명은 각 모듈 README.md를 참고해주세요.

<br/>

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcHD02o%2FbtsH8G6bEze%2FgkOXvPS5h9ZNeIdKRDl9VK%2Fimg.png)

<br/><br/><br/><br/>

# 📁 패키지 구조

core 패키지는 , common 패키지는 프로젝트에서 공통으로 사용되는 . 상위 모듈은 하위 모듈에 의존하지 않으며, 잘 변하지 않는 

```shell
.
├── dailyge-api
│     ......
│       └─ app
│           ├─ common    # 프로젝트 공통 설정
│           └─ core
│               └─ user  # 도메인            
│                   │─ external         #  외부 호출 계층(Optional) 
│                   ├─ presentation     #  Controller 계층            
│                   ├─ facade           #  퍼사드 계층(Optional)        
│                   ├─ application      #  Service 계층               
│                   └─ persistence      #  Repository 계층            
└── 

......

```

<br/><br/><br/><br/><br/><br/>

패키지 간 의존관계가 생기지 않도록 패키지 

![image]()

<br/><br/><br/><br/><br/><br/>

# Contributors

| [Youl](https://github.com/kkk5474096) | [Jun](https://github.com/unam98) | []()| []()|
| :---: | :---: | :---: |:---: |
|<img width="100" src="https://github.com/depromeet/TeumTeum-Android/assets/89737271/513cb651-bc4a-4b91-85f3-5090da6cfc4a.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">|<img width="100" src="https://www.creativefabrica.com/wp-content/uploads/2022/03/14/White-Paper-Texture-Background-Graphics-27154875-1-1-580x387.jpg">| 
|**Backend, UI**|**Backend, Infra**| | |


<br/><br/><br/><br/><br/><br/><br/>


