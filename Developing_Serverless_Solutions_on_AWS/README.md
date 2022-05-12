# Developing Serverless Solutions on AWS 학습 자료집
> 단축URL: https://bit.ly/dss-on-aws

# 실습과 Try-It-Out 연습
- [Developing Serverless Solutions on AWS - Course Supplement (OCS) (Korean)](https://explore.skillbuilder.aws/learn/course/external/view/elearning/9255/developing-serverless-solutions-on-aws-course-supplement-ocs-korean) - Developing Serverless Solutions on AWS 수업의 과정 보충 자료(OCS) 입니다. OCS는 탐색 가능한 과정 개요와 수강생이 스스로 사용하거나 수업 토론 중에 활용할 수 있는 복습 자료 및 지식 확인 문제를 제공합니다.

# 모듈 1: 서버리스 방식 고려

- [이벤트 기반 아키텍처 시작하기](https://aws.amazon.com/ko/blogs/compute/getting-started-with-event-driven-architecture/)
- [도메인 주도 설계](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&ejkGb=KOR&barcode=9788992939850)

# 모듈 2: API 기반 개발 및 동기식 이벤트 소스

- [HTTP API와 REST API 어떤것을 선택할 것인가?](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html)
- [HTTP API 작업](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api.html)
- [REST API 작업](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html)
- [Amazon CloudFront를 사용하여 헤더 기반 API Gateway 버전 관리 구현](https://aws.amazon.com/ko/blogs/compute/implementing-header-based-api-gateway-versioning-with-amazon-cloudfront/)
- [WebSocket API 개발자 가이드](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/apigateway-websocket-api.html)
  - [WebSocket API 호출](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/apigateway-how-to-call-websocket-api.html)
- [API Gateway API에 대해 설정할 엔드포인트 유형 선택](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/api-gateway-api-endpoint-types.html)

#  모듈 3: 인증, 권한 부여 및 액세스 제어 소개

- [API Gateway의 HTTP API에 대한 액세스 제어 및 관리](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/http-api-access-control.html)
- [API Gateway의 REST API에 대한 액세스 제어 및 관리](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/apigateway-control-access-to-api.html)
- [카카오 로그인으로 Amazon Cognito 연동하기](https://haandol.github.io/2021/01/31/cognito-kakao-login.html)
  - [Cognito - 카카오 인증 연동 생플코드](https://github.com/haandol/cognito-kakao-example)
- [사용자 풀에 토큰 사용](https://docs.aws.amazon.com/ko_kr/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-with-identity-providers.html)
- [When to Use Webhooks? Compared with WebSocket, Pub/Sub, and Polling.](https://hookdeck.com/webhooks/guides/when-to-use-webhooks#how-webhooks-work)

# 모듈 4: 서버리스 배포 프레임워크
![image](https://user-images.githubusercontent.com/3435720/167570880-03a77419-e96a-4d30-8b89-b2b90ccde731.png)

- 배포 프레임워크별 코드 비교
  - [CloudFormation VPC생성](https://docs.aws.amazon.com/ko_kr/codebuild/latest/userguide/cloudformation-vpc-template.html)
  - [CDK VPC생성](https://docs.aws.amazon.com/cdk/api/v2/docs/aws-cdk-lib.aws_ec2.Vpc.html)
  - [SAM 저장소(DynamoDB) 추가](https://catalog.us-east-1.prod.workshops.aws/workshops/d21ec850-bab5-4276-af98-a91664f8b161/en-US/make-updates/add-datastore)
  - [Amplify 스토리지 추가](https://docs.amplify.aws/cli/storage/overview/)

- Workshop
  - [AWS CloudFormation Workshop](https://catalog.workshops.aws/cfn101/en-US)
  - [CDK Workshop](https://cdkworkshop.com/)
  - [SAM Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/d21ec850-bab5-4276-af98-a91664f8b161/en-US)
  - [Amplify Workshop](https://master.d3f5073vvso9t3.amplifyapp.com/)

# 실습 1: 간단한 서버리스 애플리케이션 배포

- ❗주의점
  -  22번 Generate client secret 확인란 취소를 놓치게 되면 73번의 Create account에서 실패하게 됩니다.


# 모듈 7: 적절한 Lambda 함수 작성

- [.zip 또는 JAR 파일 아카이브를 사용하여 Java Lambda 함수 배포](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/java-package.html)
- [Amazon SQS에서 Lambda 사용 - 배치 항목 실패 보고](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/with-sqs.html#services-sqs-batchfailurereporting)
- [AWS Lambda에서 사용자 지정 체크포인트로 배치 처리 최적화](https://aws.amazon.com/ko/blogs/compute/optimizing-batch-processing-with-custom-checkpoints-in-aws-lambda/)
- [스트림 처리 및 비동기식 호출을 위한 새로운 AWS Lambda 제어](https://aws.amazon.com/ko/blogs/compute/new-aws-lambda-controls-for-stream-processing-and-asynchronous-invocations/)
- [Lambda EventSourceMappingConfiguration](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/API_EventSourceMappingConfiguration.html)

# 모듈 8: 오케스트레이션을 위한 Step Functions

- [AWS Step Functions - 경로](https://docs.aws.amazon.com/step-functions/latest/dg/amazon-states-language-paths.html)
- [JsonPath 구문](https://github.com/json-path/JsonPath)
- [Data flow simulator](https://us-east-1.console.aws.amazon.com/states/home?region=us-east-1#/simulator) - 경로의 작동방식을 이해하는데 있어서 크게 도움이 되는 시뮬레이터 입니다.
- [내장 함수](https://docs.aws.amazon.com/step-functions/latest/dg/amazon-states-language-intrinsic-functions.html)

# 모듈 9: 관찰 가능성 및 모니터링

- [One Observality Workshop](https://catalog.workshops.aws/observability/ko-KR)
- [API Gateway에서 REST API에 대한 CloudWatch 로깅 설정](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/set-up-logging.html)
- [Analyzing API Gateway custom access logs for custom domain names](https://aws.amazon.com/ko/blogs/compute/analyzing-api-gateway-custom-access-logs-for-custom-domain-names/)
- [CloudWatch Logs Insights 쿼리 구문](https://docs.aws.amazon.com/ko_kr/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html)
  - [샘플 쿼리](https://docs.aws.amazon.com/ko_kr/AmazonCloudWatch/latest/logs/CWL_QuerySyntax-examples.html)
- [X-ray 란 무엇인가?](https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html)
- [AWS X-ray 관련 블로그 글들](https://aws.amazon.com/ko/blogs/developer/category/developer-tools/aws-x-ray/)
- [Java용 X-Ray SDK를 사용하는 SQL 쿼리 추적](https://docs.aws.amazon.com/ko_kr/xray/latest/devguide/xray-sdk-java-sqlclients.html)
- [Amazon CodeGuru Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/1786241d-967f-4195-99ef-5716ef485201/en-US/)
- [Amazon CodeGuru](https://aws.amazon.com/ko/codeguru/)

# 모듈 11: 서버리스 애플리케이션에서 규모 조정 처리

- [Amazon API Gateway 할당량 및 중요 정보](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/limits.html)
- [HTTP API에 대한 AWS 서비스 통합 작업(1급 통합 서비스)](https://docs.aws.amazon.com/ko_kr/apigateway/latest/developerguide/http-api-develop-integrations-aws-services.html)
- [AWS Lambda Power Tuning](https://github.com/alexcasalboni/aws-lambda-power-tuning)
- [Lambda의 확장 및 동시성](https://docs.aws.amazon.com/ko_kr/lambda/latest/operatorguide/scaling-concurrency.html)
- [Lambda 프로비저닝된 동시성 관리](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/provisioned-concurrency.html)
- [Lambda 함수 크기 조정](https://docs.aws.amazon.com/ko_kr/lambda/latest/dg/invocation-scaling.html)
- [Operating Lambda: Debugging code – Part 1](https://aws.amazon.com/ko/blogs/compute/operating-lambda-debugging-code-part-1/)
- [Operating Lambda: Debugging configurations – Part 2](https://aws.amazon.com/ko/blogs/compute/operating-lambda-debugging-configurations-part-2/)
- [Operating Lambda: Debugging configurations – Part 3](https://aws.amazon.com/ko/blogs/compute/operating-lambda-debugging-integrations-part-3/)
- [Scheduling AWS Lambda Provisioned Concurrency for recurring peak usage](https://aws.amazon.com/ko/blogs/compute/scheduling-aws-lambda-provisioned-concurrency-for-recurring-peak-usage/)
- [Amazon SQS에 사용할 수 있는 CloudWatch 지표](https://docs.aws.amazon.com/ko_kr/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-available-cloudwatch-metrics.html)
- [Amazon Kinesis Data Streams, 고속 스트리밍을 위해 향상된 팬아웃 및 HTTP/2 지원 추가](https://aws.amazon.com/ko/blogs/korea/kds-enhanced-fanout/)
