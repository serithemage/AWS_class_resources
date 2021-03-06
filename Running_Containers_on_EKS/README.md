# Running Containers on EKS 수업 자료

## [쿠버네티스 용어집](https://kubernetes.io/ko/docs/reference/glossary/)

## 컨테이너 기초
- [컨테이너란? 리눅스의 프로세스 격리 기능](https://www.44bits.io/ko/keyword/linux-container)
- [컨테이너는 왜 써야 하나요?](https://www.netapp.com/ko/devops-solutions/what-are-containers/)
- [도커 이미지 빌드와 Dockerfile 기초](https://www.44bits.io/ko/post/building-docker-image-basic-commit-diff-and-dockerfile)
- [도커(Docker) 이미지의 구조](https://www.44bits.io/ko/post/how-docker-image-work)
- [도커 컨테이너는 가상머신인가요? 프로세스인가요?](https://www.44bits.io/ko/post/is-docker-container-a-virtual-machine-or-a-process)
 
## 그 밖의 자료
- [AWS 컨테이너 블로그](https://aws.amazon.com/blogs/containers/)
- [This is My Architecture - Containers](https://aws.amazon.com/architecture/this-is-my-architecture/?tma.sort-by=item.additionalFields.airDate&tma.sort-order=desc&awsf.category=categories%23containers&awsf.industry=*all&awsf.language=*all&awsf.show=*all&awsf.format=*all)

# 수업 모듈별 참고자료 정리

## 모듈 1: Kubernetes 기초
- [The Twelve-Factor Apps](https://12factor.net/ko/)
- [컨테이너와 서버리스 기술을 통한 디지털 트랜스포메이션](https://www.slideshare.net/awskorea/digital-transformation-by-container-and-servelss-technology-do-hyun-jung-2) - 마이크로 서비스와 컨테이너와의 관계 설명
- [EKS 워크숍](https://www.eksworkshop.com/)
- [Kubernetes 오브젝트 개요](https://shipit.dev/posts/kubernetes-overview-diagrams.html)
- [Multi-Container Design Patterns](https://kubernetes.io/blog/2015/06/the-distributed-system-toolkit-patterns/)
- [EKS에서 영구 스토리지 사용하기](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-persistent-storage/)
- [테인트(TAINTS) 및 톨러레이션(TOLERATIONS)](https://access.redhat.com/documentation/ko-kr/openshift_container_platform/4.6/html/post-installation_configuration/post-install-taints-tolerations)
- [톨러레이션(TOLERATIONS)의 operator와 effect](https://wrapitup.tistory.com/2) 
- [Build a Kubernetes Operator in six steps](https://developers.redhat.com/articles/2021/09/07/build-kubernetes-operator-six-steps)
- [OperatorHub.io](https://operatorhub.io/)

## 모듈 2: EKS 기초
- [eksctl로 관리형 노드 그룹 생성](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/create-managed-node-group.html)

## 모듈 3: 클러스터 생성
- [eksctl - The official CLI for Amazon EKS](https://eksctl.io/)
  - [Amazon EKS 시작하기 - eksctl](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/getting-started-eksctl.html)
- [CDK EKS module](https://docs.aws.amazon.com/cdk/api/v1/docs/aws-eks-readme.html)
- [CDK8S - Cloud Development Kit for Kubernetes](https://cdk8s.io/)
- [AWS CloudFormation - AWS::EKS::Cluster](https://docs.aws.amazon.com/ko_kr/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)
- [Terraform EKS module](https://registry.terraform.io/modules/terraform-aws-modules/eks/aws/latest)
  - [Provision an EKS Cluster](https://learn.hashicorp.com/tutorials/terraform/eks)
- [AWS CLI Command Reference - EKS](https://docs.aws.amazon.com/cli/latest/reference/eks/index.html)
- [Amazon EKS용 kubeconfig 생성](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/create-kubeconfig.html)
- [Cluster Autoscaler 배포](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/autoscaling.html)
  - [클러스터에 대한 IAM OIDC 공급자 생성](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/enable-iam-roles-for-service-accounts.html)  

### 실습 1 도전과제
 K9S를 설치하고 사용해 봅시다.
 
 - [k9s](https://github.com/derailed/k9s) - 터미널기반 쿠버네티스 대쉬보드
  - [k9s 명령어](https://k9scli.io/topics/commands/)
  - [처음 시작하는 분을 위한 k9s 기초 사용법](https://1minute-before6pm.tistory.com/18)
 
 설치법
 ```bash
 touch ~/.bashrc
 curl -sS https://webinstall.dev/k9s | bash
 source ~/.bashrc
 
 k9s
 ```

## 모듈 4: 애플리케이션 배포

### [데모: Amazon ECR 구성하기](https://docs.aws.amazon.com/ko_kr/AmazonECR/latest/userguide/repository-create.html)
- [ECR 프라이빗 리포지토리 생성](https://docs.aws.amazon.com/ko_kr/AmazonECR/latest/userguide/repository-create.html)
  - [이미지 스캔](https://docs.aws.amazon.com/ko_kr/AmazonECR/latest/userguide/image-scanning.html)
    - [고급 스캔](https://docs.aws.amazon.com/ko_kr/AmazonECR/latest/userguide/image-scanning-enhanced.html)
    - [기본 스캔](https://docs.aws.amazon.com/ko_kr/AmazonECR/latest/userguide/image-scanning-basic.html)
   - [44bits - 아마존 ECR, 도커 이미지 취약점 스캔 기능 추가](https://www.44bits.io/ko/post/news--amazon-ecr-docker-image-vulnerabilities-scanning)
### [데모: Helm을 사용하여 애플리케이션 배포하기](https://www.eksworkshop.com/beginner/060_helm/helm_nginx/installnginx/)
- [Bitnami NginX Helm Chart](https://github.com/bitnami/charts/tree/master/bitnami/nginx)

## 모듈 5: 가시성
- [EKS Workshop - Monitoring using Prometheus and Grafana](https://www.eksworkshop.com/intermediate/240_monitoring/)
  - [Grafana Dashboards](https://grafana.com/grafana/dashboards/)
- [Container Insights 사전 조건 확인](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-prerequisites.html)
- [Amazon EKS 및 Kubernetes에서 Container Insights의 빠른 시작 설정](https://docs.aws.amazon.com/ko_kr/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-EKS-quickstart.html)
- [EKS Workshop - Container Insight](https://www.eksworkshop.com/intermediate/250_cloudwatch_container_insights/)
- [Fargate기반 EKS클러스터에서 Fluent Bit로그 수집](https://aws.amazon.com/blogs/containers/fluent-bit-for-amazon-eks-on-aws-fargate-is-here/)

## 모듈 6: 효율성, 복원력, 비용 최적화 간의 균형 유지
- [AWS Well-Architected 프레임워크](https://wa.aws.amazon.com/index.ko.html)
- [Amazon EKS에서 EC2 스팟 인스턴스를 사용하는 모범 사례는 무엇인가요?](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-spot-instance-best-practices/)
- [How to track costs in multi-tenant Amazon EKS clusters using Kubecost](https://aws.amazon.com/ko/blogs/containers/how-to-track-costs-in-multi-tenant-amazon-eks-clusters-using-kubecost/)
- [EKS Workshop - OPTIMIZED WORKER NODE MANAGEMENT WITH OCEAN BY SPOT.IO](https://www.eksworkshop.com/beginner/190_ocean/)
- [PodDisruptionBudget](https://kubernetes.io/docs/concepts/workloads/pods/disruptions/#pod-disruption-budgets)
  - [Specifying a Disruption Budget for your Application](https://kubernetes.io/docs/tasks/run-application/configure-pdb/)

## 모듈 7: 네트워킹
- [포드 네트워킹(CNI)](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/pod-networking.html)
- [쿠버네티스 네트워킹](https://kubernetes.io/ko/docs/concepts/services-networking/)
- AWS App Mesh
  - [AWS App Mesh 와 Kubernetes 연동](https://docs.aws.amazon.com/ko_kr/app-mesh/latest/userguide/getting-started-kubernetes.html)
  - [AWS App Mesh, 회로 차단기 기능 도입](https://aws.amazon.com/ko/about-aws/whats-new/2020/11/aws-app-mesh-introduces-circuit-breaker-capabilities/)
  - [AWS App Mesh Workshop](https://www.appmeshworkshop.com/)
  - [AWS App Mesh 및 Amazon EKS 시작하기](https://aws.amazon.com/ko/blogs/containers/getting-started-with-app-mesh-and-eks/)

## 모듈 8: 보안 인증
![image](https://user-images.githubusercontent.com/3435720/162117897-43ebd723-fff8-4d08-82d2-0386c448c781.png)

- [클러스터에 대한 IAM OIDC 공급자 생성](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/enable-iam-roles-for-service-accounts.html)
- [IAM 역할을 서비스 계정에 연결](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/specify-service-account-role.html)
- [AWS EKS Service Account에 AWS IAM Role 부여](https://ssup2.github.io/theory_analysis/AWS_EKS_Service_Account_IAM_Role/)
- [Amazon EKS 클러스터의 IAM 사용자에 대해 여러 네임스페이스에 걸친 권한을 관리하려면 어떻게 해야 합니까?](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-iam-permissions-namespaces/)
- [Apache Log4j 취약점으로부터 Kubernetes 워크로드 보호](https://aws.amazon.com/ko/blogs/containers/protect-kubernetes-workloads-from-apache-log4j-vulnerabilities/)
- [Java 기반 워크로드 운영자를 위한 Amazon EKS에서 Kubernetes RBAC 및 IAM 통합](https://aws.amazon.com/ko/blogs/containers/kubernetes-rbac-and-iam-integration-in-amazon-eks-using-a-java-based-kubernetes-operator/)
- [Amazon EKS 클러스터의 특정 IP 주소에 대한 API 액세스를 잠그려면 어떻게 해야 합니까?](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-lock-api-access-IP-addresses/)
- [AWS App Mesh와 함께 Amazon EKS에서 사이드카 삽입 사용](https://aws.amazon.com/ko/blogs/containers/using-sidecar-injection-on-amazon-eks-with-aws-app-mesh/)
- [Amazon EKS 클러스터에 대한 멀티 테넌트 설계 고려 사항](https://aws.amazon.com/blogs/containers/multi-tenant-design-considerations-for-amazon-eks-clusters/)

## 모듈 9: 보안 워크플로우
- [VXLAN이란?](https://www.juniper.net/kr/ko/research-topics/what-is-vxlan.html)
- [Amazon EKS에 Calico 설치](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/calico.html)
- [Kubernetes Secrets](https://kubernetes.io/ko/docs/concepts/configuration/secret/)

### 실습 5 관련
- [CloudWatch Logs 쿼리 문법](https://docs.aws.amazon.com/ko_kr/AmazonCloudWatch/latest/logs/CWL_QuerySyntax.html)

## 모듈 10: 업그레이드
- [Kubernetes 릴리스 히스토리](https://kubernetes.io/ko/releases/)
- [EKS Kubernetes 버전](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/kubernetes-versions.html)
- [Amazon EKS 클러스터 Kubernetes 버전 업데이트 가이드 문서](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/update-cluster.html)
- [[고객 사례 소개] 하이퍼커넥트 - Terraform 을 이용한 EKS upgrade](https://wonderwal1.notion.site/EKS-Cluster-Upgrade-with-terraform-dfe2281e6e97446cb4c45f7cad2e5a42)
- [Safely Drain a Node](https://kubernetes.io/docs/tasks/administer-cluster/safely-drain-node/)
- [flagger](https://github.com/fluxcd/flagger) - Flagger는 Kubernetes에서 실행되는 애플리케이션의 릴리스 프로세스를 자동화하는 점진적 전달 도구입니다. 메트릭을 측정하고 적합성 테스트를 실행하는 동안 트래픽을 새 버전으로 점진적으로 이동하여 프로덕션에 새 소프트웨어 버전을 도입할 위험을 줄입니다.

