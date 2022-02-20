# Running Containers on EKS 수업 자료

## [쿠버네티스 용어집](https://kubernetes.io/ko/docs/reference/glossary/)

- [k9s](https://github.com/derailed/k9s) - 터미널기반 쿠버네티스 대쉬보드
  - [k9s 명령어](https://k9scli.io/topics/commands/)

## 모듈1
- [The Twelve-Factor Apps](https://12factor.net/ko/)
- [EKS 워크숍](https://www.eksworkshop.com/)
- [Kubernetes 오브젝트 개요](https://shipit.dev/posts/kubernetes-overview-diagrams.html)
- [Multi-Container Design Patterns](https://kubernetes.io/blog/2015/06/the-distributed-system-toolkit-patterns/)
- [EKS에서 영구 스토리지 사용하기](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-persistent-storage/)
- [테인트(TAINTS) 및 톨러레이션(TOLERATIONS)](https://access.redhat.com/documentation/ko-kr/openshift_container_platform/4.6/html/post-installation_configuration/post-install-taints-tolerations)
- [톨러레이션(TOLERATIONS)의 operator와 effect](https://wrapitup.tistory.com/2) 
- [Build a Kubernetes Operator in six steps](https://developers.redhat.com/articles/2021/09/07/build-kubernetes-operator-six-steps)
- [OperatorHub.io](https://operatorhub.io/)

## 모듈3 - 클러스터 생성
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

## 모듈10 - 업그레이드
- [Kubernetes 릴리스 히스토리](https://kubernetes.io/ko/releases/)
- [EKS Kubernetes 버전](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/kubernetes-versions.html)
- [Amazon EKS 클러스터 Kubernetes 버전 업데이트 가이드 문서](https://docs.aws.amazon.com/ko_kr/eks/latest/userguide/update-cluster.html)
- [Terraform 을 이용한 EKS upgrade](https://wonderwal1.notion.site/EKS-Cluster-Upgrade-with-terraform-dfe2281e6e97446cb4c45f7cad2e5a42)
- [PodDisruptionBudget](https://kubernetes.io/docs/concepts/workloads/pods/disruptions/#pod-disruption-budgets)
  - [Specifying a Disruption Budget for your Application](https://kubernetes.io/docs/tasks/run-application/configure-pdb/)
- [Safely Drain a Node](https://kubernetes.io/docs/tasks/administer-cluster/safely-drain-node/)

## 보안
- [Apache Log4j 취약점으로부터 Kubernetes 워크로드 보호](https://aws.amazon.com/ko/blogs/containers/protect-kubernetes-workloads-from-apache-log4j-vulnerabilities/)
- [Java 기반 워크로드 운영자를 위한 Amazon EKS에서 Kubernetes RBAC 및 IAM 통합](https://aws.amazon.com/ko/blogs/containers/kubernetes-rbac-and-iam-integration-in-amazon-eks-using-a-java-based-kubernetes-operator/)
- [Amazon EKS 클러스터의 특정 IP 주소에 대한 API 액세스를 잠그려면 어떻게 해야 합니까?](https://aws.amazon.com/ko/premiumsupport/knowledge-center/eks-lock-api-access-IP-addresses/)
