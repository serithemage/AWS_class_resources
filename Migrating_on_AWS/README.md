# Migrating to AWS

# 1일 차

## 모듈 1: 클라우드 마이그레이션이란 무엇입니까?

## 모듈 2: 마이그레이션 준비 상태 평가

- [AWS 마이그레이션 평가기](https://aws.amazon.com/migration-evaluator/)
  - [평가기 실행 보고서 샘플](https://d1.awsstatic.com/asset-repository/Migration_Evaluator_Quick_Insights_Sample_Report.pdf)


## 모듈 3: 마이그레이션 준비 및 관련 작업 이해 

## 모듈 4: 랜딩 존 및 이점 파악

## 모듈 5: 랜딩 존 구축

## 모듈 6: 포트폴리오 검색 및 마이그레이션 전략 이해 

## 실습 1: 온프레미스 네트워크 및 디렉터리 서비스를 AWS에 연결

이 실습에서는 AWS Transit Gateway 및 AWS Site-to-Site VPN을 사용하여 온프레미스 환경을 AWS에 연결하는 방법을 소개합니다. 또한 AD Connector를 사용하여 온프레미스 Active Directory 환경을 AWS에 연결하는 방법을 보여줍니다. 마지막으로 AD Connector를 사용하여 AWS 관리 콘솔 및 EC2 도메인 조인에 페더레이션 로그인을 제공하는 방법을 보여줍니다.

### 실습 팁(모든 실습 공통)
1. 손에 익은 텍스트 에디터를 하나 열어놓고 실습을 진행하세요.
2. 윈도우 인스턴스 접속시 과카몰대신 RDP 클라이언트를 이용하세요.

# 2일 차

## 모듈 7: 포트폴리오 검색 도구 이해 및 선택

## 실습 2: 마이그레이션에 필요한 애플리케이션 데이터 수집

## 모듈 8: 마이그레이션 계획 및 설계

## 모듈 9: AWS로의 마이그레이션 수행

## 실습 3: 애플리케이션을 AWS로 마이그레이션

- 14번: 다음 명령에서 [activation_code], [activation_id] 및 [labRegion] 을 바꾸고, PowerShell 창에 붙여넣은 다음 Enter 키를 누릅니다.
    
    ```bash
    아래 Activation Code 및 ID는 실습 환경에 맞게 변경해야합니다.(반드시 copy해 두세요)
    
    Activation Code   5m9VdHfl3VFBJdzpZKDp
    Activation ID   33fe15d2-6f08-418b-9bd3-c2f5cc08622c
    ```
    
    ```powershell
    Windows
    $code = "[activation_code]"
    $id = "[activation_id]"
    $region = "[labRegion]"
    -----------------------------
    $code = "5m9VdHfl3VFBJdzpZKDp"
    $id = "33fe15d2-6f08-418b-9bd3-c2f5cc08622c"
    $region = "us-west-2"
    ```
    
- 30번: 다음 명령에서 [activation_code], [activation_id] 및 [Region] 을 바꾸고, Instance Connect 창에 붙여넣은 다음 Enter 키를 누릅니다.
    
    ```bash
    Linux
    code=[activation_code]
    id=[activation_id]
    region=[labRegion]
    ----------------------------
    code=5m9VdHfl3VFBJdzpZKDp
    id=33fe15d2-6f08-418b-9bd3-c2f5cc08622c
    region=us-west-2
    ```
 - 15번이나 31번 명령어를 두 번 실행하면 인스턴스가 여러대 등록합니다. 이 경우엔 FleetManagement에서 중복된 인스턴스를 등록 해제 해 주세요. 등록 해제 방법은 20번과 36번 바로 아래 !중요 부분에 정리되어 있습니다.

## 모듈 10: 데이터베이스 및 데이터 마이그레이션 서비스 이해

## 실습 4: 기존 데이터베이스를 Amazon Aurora로 마이그레이션

