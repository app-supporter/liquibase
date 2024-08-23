
# Dailyge Infra

Dailyge Infra 저장소 입니다. 

<div align="center">
  <img width="400" src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FCl3Zr%2FbtsH9tFrQxe%2F4Wd1nL8FuHANpzi9flDwBK%2Fimg.png"><br/><br/>
</div>
  
<div align="center">
  
  Dailyge로 하루 일정 관리를 간편하게! <br>
  🏃 성실한 하루의 연속이 큰 변화를 가져옵니다.

  [![Release](https://img.shields.io/badge/-📚_API_Docs-brightgreen)]() [![Release](https://img.shields.io/badge/-📚_Team_Blog-blue)]() <br/>
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()
  [![Release](https://img.shields.io/badge/%E2%9C%A8%20release-v1.0.0-brightgreen)]()

</div>

<br/><br/><br/><br/><br/><br/>

# 1. Table of Contents.

1. 서비스 소개
2. Skills
3. CICD
4. Architecture
5. Moduels
6. Package


<br/><br/><br/><br/>

## 패키지 구조

```shell
├─ README.md
├─ main.tf
├─ 📁modules                  # Modules
│       ├─📁 cloudfront       # Resource
│       │    └── ......
│       ├─📁 s3
│       │    └── ......
│       └─📁 vpc
│           ├─ main.tf        # main.tf
│           ├─ output.tf      # output.tf
│           └─ variables.tf   # variables.tf
├── variable.tf
└── variables.tf
```

> 명시적으로 dev, prod 패키지를 나누었지만 규모가 작기 때문에 dev 하나만 사용하고 있으며, 동일 이유로 Atlantis도 사용하지 않았습니다.

<br/><br/><br/><br/><br/><br/>

# 2. Skills.

서비스 구축을 위해 AWS를 활용했으며, 모니터링은 Prometheus와 Grafana를 사용하고 있습니다. 운영 로그 및 시스템 로그는 모두 AWS CloudWatch로 관리하고 있으며, 운영 과정에서 발생하는 이슈는 Grafana Alert Rule 또는 AWS Lambda로 보고받고 있습니다. 비용 절감을 위해 일부 서버는 Google Cloud를 활용하고 있습니다. Terraform으로 관리되는 자원은 Route53, CloudFront, S3, ALB, ECS, EC2(Backend), RDS 입니다. 모든 자원을 코드로 관리 하지는 않으며, 일부 자원들은 설치형으로 사용하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbcU6So%2FbtsH8Nkm8aQ%2FEneyp26AkfimW78whEvwmK%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

## 👬 Collaboration.

협업 툴은 이슈 트래킹을 위해 Jira/Confluencer를, 자동화 툴은 Zapier와 GitAction을 사용하고 있습니다. 팀원 간 커뮤니케이션은 Slack으로 이루어지며, 또한 CICD 과정에서 발생한 리포트, AWS 비용 결과도 Slack으로 보고 받고 있습니다. 팀원 간 코드 컨벤션 관리 및 코드 스멜 제거를 위해 CheckStlye, PMD, SpotBugs, Sonarqube, Codev와 같은 정적 코드 분석 툴을 도입했습니다. 

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FS4C8q%2FbtsIaFkRVfB%2FLL4VJpYGVJZLMKi6h5yed1%2Fimg.png)

> 팀 규칙 및 기술 관련 글은 문서 관리의 용이성을 위해 [Gitbook]()을 사용하고 있습니다.


# 3. CICD

PR이 생성되면 자동으로 정적 분석을 시작하며, Slack으로 결과를 보고받습니다. 팀원 간 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 개발 서버로 배포가 되며, 인수 테스트가 시작됩니다. 자동 인수 테스트 외에도 QA를 진행하며 기능의 동작 유무, 버그 리포팅을 합니다. main 브랜치로 병합이 되면 상용 서버로 배포가 되며, 최종 결과를 보고받습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

테스트, 배포 결과 및 AWS 비용은 슬랙을 통해 확인하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F57TWx%2FbtsJdr7XsmA%2FfihnO93ztuKmPq960lSp71%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

Route53에서 WAF로 사용자 최대 사용자 요청을 제한하고 있으며, 모니터링 서버, 관리자 API 등 특정 리소스에 대한 접근은 ALB와 WAF, Security Group으로 제한하고 있습니다.

![image]()

<br/><br/><br/><br/><br/><br/>

모니터링은 Prometheus와 Grafana를 CloudWatch와 연동해 사용하고 있으며, 이를 통해 알림을 받고 있습니다. 

![image]()

<br/><br/><br/><br/>

모니터링 중인 자원은 EC2 서버, 애플리케이션, RDS, Redis, MongoDB 이며, CPU/메모리 사용률, Slow Query 등을 체크하고 있습니다.

![image]()
