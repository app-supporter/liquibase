
# Dailyge Infra

Dailyge Infra 저장소 입니다. 

<div align="center">
  <img width="400" src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FCl3Zr%2FbtsH9tFrQxe%2F4Wd1nL8FuHANpzi9flDwBK%2Fimg.png"><br/><br/>
</div>
  
<div align="center">
  
  Dailyge Infra 저장소 입니다.  <br>
  서비스 소개는 [해당 링크]()를 참조해주세요. 😃 

</div>

<br/><br/><br/><br/><br/><br/>

# Table of Contents.

1. Skills
2. CICD
3. Architecture
4. Package


<br/><br/><br/><br/>

# 1. Skills.

서비스 구축을 위해 AWS를 활용했으며, Terraform을 사용해 자원을 프로비저닝 했습니다. Terraform으로 관리되는 자원은 Route53, CloudFront, S3, ALB, ECS, EC2(Application), RD 이며, 일부 자원들은 설치형으로 사용하고 있습니다. 모니터링은 Prometheus와 Grafana를 사용하고 있으며, 운영 및 시스템 로그는 모두 AWS CloudWatch로 관리하고 있습니다. 운영 과정에서 발생하는 이슈는 Grafana Alert 또는 AWS Lambda를 통해 슬랙으로 보고받고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FY5ifk%2FbtsJeVnHEJH%2FyQlxRPikUxlOzPKbyUs2Fk%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

# 2. CICD

PR이 생성되면 자동으로 정적 분석을 시작하며, Slack으로 결과를 보고받습니다. 팀원 간 코드 리뷰를 거친 후, dev 브랜치로 병합이 되면 개발 서버로 배포가 되며, 인수 테스트가 시작됩니다. 자동 인수 테스트 외에도 QA를 진행하며 기능의 동작 유무, 버그 리포팅을 합니다. main 브랜치로 병합이 되면 상용 서버로 배포가 되며, 최종 결과를 보고받습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fr93f9%2FbtsH8AyHS2Z%2FGkQyAVeysys35m6sR5fhA1%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

테스트, 배포 결과 및 비용은 슬랙을 통해 확인하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F57TWx%2FbtsJdr7XsmA%2FfihnO93ztuKmPq960lSp71%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

# 3. Architecture

정적 자원은 S3와 CloudFront를, 서버 오케스트레이션은 AWS ECS를 사용했습니다. 각 리소스는 VPC 내부 별도의 서브넷(Public/Private)에 존재하며, ALB와 NAT를 통해 외부와 통신합니다.  

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdsaShw%2FbtsJemzlzQi%2FfmxkJnzC00ay1kAkxcZir1%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

Route53에서 WAF로 일정 시간 동안 최대 사용자 요청을 제한하고 있으며, 모니터링 서버, 관리자 API 등 특정 리소스에 대한 접근은 ALB와 WAF, Security Group으로 제한하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fmm1Pm%2FbtsJen4PTWG%2FR6WvrLH2vsZAu2Jb0x05t0%2Fimg.png)

<br/><br/><br/><br/><br/><br/>

모니터링은 Prometheus와 Grafana를 CloudWatch와 연동해 사용하고 있으며, 이를 통해 알림을 받고 있습니다. 모니터링 중인 리소스는 EC2 서버, 애플리케이션 지표, RDS, Redis, MongoDB 이며, CPU/메모리 사용률, Slow Query 등을 체크하고 있습니다.

![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FeEeYh0%2FbtsJfPz2TdW%2FDD2Zu0zqkZfkljdEFs7960%2Fimg.png)

> 애플리케이션이 다운될 경우, 자동으로 힙 덤프를 뜬 후, 이를 정적 저장소로 업로드하고 알림을 보내고 있습니다.

<br/><br/><br/><br/><br/><br/>

## 패키지 구조

modules 내부에 개발 환경을 기준으로 파일을 구분하고 있습니다. 명시적으로 dev, prod 패키지를 나누었지만 프로젝트 규모가 작기 때문에 dev 하나만 사용하고 있습니다. 

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

> Atlantis는 별도의 서버가 필요하기 때문에, 프로젝트 규모를 고려해 사용하지 않았습니다.


<br/><br/><br/><br/><br/><br/>

애플리케이션이 다운될 경우, 자동으로 힙 덤프를 뜨며, 이를 외부 저장소로 전송하고 있습니다. 

![image]()
