# bit.ly/dev-on-aws-resource </br> Developing on AWS(AWS 기반 개발 v4.x) 수업 자료 

> Developing on AWS ver 3.x 를 위한 수업자료는 [여기](DevOnAWS_v3.md)를 클릭 하세요

## Module 1 - 과정 개요

### AWS 개발 관련 디지털 강의
  - [AWS Cloud Practitioner Essentials (Korean)](https://explore.skillbuilder.aws/learn/course/external/view/elearning/1928/aws-cloud-practitioner-essentials-korean) - 이 과정은 특정 기술 역할과 관계없이 Amazon Web Services(AWS) 클라우드를 전반적으로 이해하려는 개인을 대상으로 합니다. AWS 클라우드에 대한 지식을 쌓을 수 있도록 AWS 클라우드 개념, AWS 서비스, 보안, 아키텍처, 요금 및 지원에 대해 배우게 됩니다. 또한 이 과정은 AWS 공인 클라우드 전문가 시험을 준비하는 데 도움이 됩니다.
  - [Introduction to Serverless Development (Korean)](https://explore.skillbuilder.aws/learn/course/external/view/elearning/940/introduction-to-serverless-development-korean) - 이 과정에서는 서버리스 애플리케이션의 개발을 시작하는 데 도움이 되는 주요 서버리스 개념을 소개합니다. 서버 기반 개발에서 이미 사용하고 있는 개발 모범 사례를 어떻게 서버리스 개발에도 그대로 적용하는지, 그리고 서버리스 애플리케이션 개발에 적합한 개발 프로세스를 알아봅니다.
  - [Developing Serverless Solutions on AWS (Korean) - 8시간](https://explore.skillbuilder.aws/learn/course/external/view/elearning/10460/developing-serverless-solutions-on-aws-korean) - 이 과정에서는 개발자가 AWS Lambda 및 AWS 서버리스 플랫폼의 다른 서비스를 사용하여 서버리스 애플리케이션을 구축하는 모범 사례를 살펴보고 연습할 수 있습니다. 과정 내내 AWS 설명서를 사용하여 강의실 밖에서도 학습 및 문제 해결을 달성할 수 있는 실제적 방법을 습득하게 됩니다.
  - [Developing Serverless Solutions on AWS - Course Supplement (OCS) (Korean)](https://explore.skillbuilder.aws/learn/course/external/view/elearning/9255/developing-serverless-solutions-on-aws-course-supplement-ocs-korean) - Developing Serverless Solutions on AWS 수업의 과정 보충 자료(OCS) 입니다. OCS는 탐색 가능한 과정 개요와 수강생이 스스로 사용하거나 수업 토론 중에 활용할 수 있는 복습 자료 및 지식 확인 문제를 제공합니다.

### AWS 개발 관련 학습 리소스 
- [The Twelve Factor App](https://12factor.net/ko/)
- [AWS Training](https://aws.training)
- [AWS News Blog](https://aws.amazon.com/ko/blogs/aws/)
- [edX AWS Online Course](https://www.edx.org/school/aws)
- 실습
  - [최신 실습 콘텐츠 찾아보기](https://www.google.com/search?q=aws+workshop)
  - https://workshops.aws
  - https://awsworkshop.io
  - [AWS 한국어 실습 가이드](https://aws.amazon.com/ko/blogs/korea/aws-korean-hands-on-labs-guides/)
- [클론 코딩](https://www.youtube.com/watch?v=yu7GQ4zbTsw)
- [취미생활을 위한 AWS 활용법](https://bit.ly/aws-for-hobby)

## Module 2 - AWS에 웹 애플리케이션 구축

- [언어별 개발자 도구(SDK)](https://aws.amazon.com/ko/tools/)
- [AWS CLI](https://aws.amazon.com/ko/cli/)
- AWS Toolkit
  - [AWS Toolkit for Visual Studio Code](https://aws.amazon.com/visualstudiocode/)
  - [AWS Toolkit for Eclipse](https://aws.amazon.com/ko/eclipse/)
  - [AWS Toolkit for JetBrains](https://docs.aws.amazon.com/ko_kr/toolkit-for-jetbrains/latest/userguide/welcome.html)
  - [AWS Toolkit for Visual Studio](https://docs.aws.amazon.com/ko_kr/toolkit-for-visual-studio/latest/user-guide/welcome.html)
- AWS SAM
  - [AWS SAM 자습서: Hello World 애플리케이션 배포](https://docs.aws.amazon.com/ko_kr/serverless-application-model/latest/developerguide/serverless-getting-started-hello-world.html)
  - [AWS SAM Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/d21ec850-bab5-4276-af98-a91664f8b161/en-US)
  - [AWS SAM CLI Application Templates](https://github.com/aws/aws-sam-cli-app-templates)
- AWS X-Ray
  - [AWS X-Ray 처음 시작 문서](https://docs.aws.amazon.com/ko_kr/xray/latest/devguide/xray-gettingstarted.html)
 
 ## Module 3 - AWS에서 개발 시작하기
 - [OpenTelemetry](https://opentelemetry.io/) - 오픈소스 트레이스 도구. AWS X-Ray를 지원함.
 - [Cloud9 저장 공간 늘리기](https://docs.aws.amazon.com/ko_kr/cloud9/latest/user-guide/move-environment.html)
 - 버전 잠금 - 일부 AWS 서비스는 이전 버전과의 호환성을 지원하기 위해 여러 개의 API 버전을 유지하고 있습니다. 기본적으로 AWS SDK는 가장 최근에 출시된 API 버전을 사용합니다. 아래 링크에서는 SDK및 CLI에서 API버전을 고정시키기 위한 방법을 소개하고 있습니다.
   - [구성 및 자격 증명 파일 설정](https://docs.aws.amazon.com/ko_kr/cli/v1/userguide/cli-configure-files.html)
   - [JavaScript SDK의 API 버전잠금](https://docs.aws.amazon.com/ko_kr/sdk-for-javascript/v2/developer-guide/locking-api-versions.html)
 
 ## Module 4 - AWS 권한 시작하기
 
 ### 데모: 권한 테스트(AWS Management Console) - CloudShell 상에서 역할 전환하기
   > 주의사항! CloudSehll은 ECS상에서 동작하기 때문에 역할 수임을 위한 ~/.aws/config 파일 설정에서 source_profile대신에 credential_source를EcsContainer로 설정해야함(아래 코드 블럭 참고). 나머지는 아래 링크의 [AWS CLI에서 IAM Role 전환하기](https://dev.classmethod.jp/articles/aws-cli-iam-role-switch-kr/)와 동일함.

```bash
[profile role]
credential_source=EcsContainer
mfa_serial = arn:aws:iam::xxxxxxxxxxxxx:mfa/사용자명 
role_arn = arn:aws:iam::yyyyyyyyyyyy:role/역할명
```
 - [AWS CLI에서 IAM Role 전환하기](https://dev.classmethod.jp/articles/aws-cli-iam-role-switch-kr/) - 이 글에서는 역할 전환시 MFA를 사용하도록 되어 있음.
 - 그 밖의 데모 관련 참고 문서
   - [AWS CloudShell 작업](https://docs.aws.amazon.com/ko_kr/cloudshell/latest/userguide/working-with-cloudshell.html)
   - [AWS CLI에서 IAM 역할 사용](https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/cli-configure-role.html)
   - [IAM 역할을 사용하여 Amazon EC2 인스턴스에서 실행되는 애플리케이션에 권한 부여
](https://docs.aws.amazon.com/ko_kr/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html)
 
## Module 5 - 스토리지 옵션(Amazon S3 중심)

- [AWS General Immersion Day - Amazon S3 실습](https://catalog.workshops.aws/general-immersionday/ko-KR/basic-modules/60-s3/s3)

## Module 6 - 스토리지 작업 처리

- 각 언어별 SDK의 S3 샘플 코드
  - [Python](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/s3-examples.html)
  - [Java](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/examples-s3.html)
  - [.net](https://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/s3-apis-intro.html)
  - [JavaScript](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/javascript_s3_code_examples.html)
- [S3 객체의 배치 작업을 원큐에 – S3 batch operation 소개](https://wisen.co.kr/pages/blog/blog-detail.html?idx=11928)

## Module 7 - 데이터 베이스 시작하기

- [적응형 용량을 통해 DynamoDB에서 균일하지 않은 데이터 액세스 패턴을 수용하는 방법](https://aws.amazon.com/ko/blogs/korea/how-amazon-dynamodb-adaptive-capacity-accommodates-uneven-data-access-patterns-or-why-what-you-know-about-dynamodb-might-be-outdated/)
- [PartiQL - Amazon DynamoDB용 SQL 호환 쿼리 언어](https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/ql-reference.html)
- 각 언어별 SDK의 DynamoDB 샘플 코드
  - [Python](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/dynamodb.html)
    - [dynamodb-mapper](https://pypi.org/project/dynamodb-mapper/)
  - [Java](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/examples-dynamodb.html)
    - [Java: DynamoDBMapper](https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/DynamoDBMapper.html)
  - [.net](https://docs.aws.amazon.com/sdk-for-net/v3/developer-guide/dynamodb-intro.html)
  - [JavaScript](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/javascript_dynamodb_code_examples.html)
    - [Amazon DynamoDB DataMapper For JavaScript](https://github.com/awslabs/dynamodb-data-mapper-js)

## Module 8 - 데이터 베이스 작업 처리

- DynamoDB
  - [읽기/쓰기 모드](https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html#HowItWorks.ProvisionedThroughput.Manual)
  - [스캔작업](https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/Scan.html)
  - [조건식](https://docs.aws.amazon.com/ko_kr/amazondynamodb/latest/developerguide/Expressions.ConditionExpressions.html)

## Module 9 - 에플리케이션 로직 처리

- Lambda
  - [Lambda 함수 한도](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/gettingstarted-limits.html)
  - [Lambda 함수 리모트 디버깅](https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/serverless-apps-run-debug-no-template.html)

### 데모 - Lambda 함수 만들기
  - [샘플 코드](https://github.com/awsdocs/aws-lambda-developer-guide)
  - [콘솔로 Lambda 함수 생성](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/getting-started-create-function.html)
  - [컨테이너 이미지로 정의된 함수 생성](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/gettingstarted-images.html)


## Module 10 - API 관리

- [HTTP API와 REST API 중에서 선택](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/http-api-vs-rest.html)
- [WebSocket Sample App](https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:729047367331:applications~simple-websockets-chat-app)
- [API GW 매핑 템플릿](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html)
  
## Module 11 - 마이크로서비스
- [App Modernization Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/f2c0706c-7192-495f-853c-fd3341db265a/en-US/)
- [컨테이너와 서버리스 기술을 통한 디지털 트랜스포메이션](https://www.slideshare.net/awskorea/digital-transformation-by-container-and-servelss-technology-do-hyun-jung-2)
- [도커 한방에 정리(실습 포함) - 드림코딩](https://www.youtube.com/watch?v=LXJhA3VWXFA)
