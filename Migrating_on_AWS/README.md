# Migrating to AWS

## 실습 내용 녹화: http://bit.ly/tc-migration


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
 - 15번이나 31번 명령어를 두 번 실행하면 인스턴스가 여러대 등록합니다. 이 경우엔 FleetManagement에서 중복된 인스턴스를 등록 해제 해 주세요. 등록 해제 방법은 20번과 36번 바로 아래 **!중요** 섹션에 정리되어 있습니다.

<aside>
💡 Online 으로 정상적으로 표기되면 InstanceID 를 선택하고, 다음 37번 내용을 바로 진행하면 됩니다.

Online 상태임에도 Deregister this managed instance를 하면 안됩니다.

</aside>

## 실습 3: **애플리케이션을 AWS로 마이그레이션**

- 5번: 새로운 계정 등록을 위해 여기 로 이동후 화면 오른쪽에 Register for a CloudEndure Migration account를 확장한 후 다음과 같이 구성하십시오.
    ![image](https://user-images.githubusercontent.com/3435720/161693234-86c01a32-2253-49f1-aad5-3dc5318fdee6.png)

    ![image](https://user-images.githubusercontent.com/3435720/161693263-5d28350f-9d51-4fea-9c47-3b97ab1dbd31.png)
 
### **과제 1.1: 마이그레이션 프로젝트를 만들고 AWS 계정에 연결**

- 8번: 다음 값을 입력합니다.
- Project name에 을 입력합니다.
- Project type 항목이 보이면, Migration을 선택합니다. (항목이 보이지 않으면, 스킵 하시면 됩니다.)
: 아래와 같이 CloudEndure 에서 Project 를 만들 때 브라우저의 종류나 버전에 따라 화면이 다소 다를 수 있습니다.(아래 예제의 경우엔 Firefox 와 Chrome 이 동일한 화면을 보여주고 있음.
    
![image](https://user-images.githubusercontent.com/3435720/161693312-4178f2a7-0296-4f17-912e-132b5946c510.png)

    
- 14번.Migration Source 및 Migration Target에서 이 지침 왼쪽에 있는 Region 값과 일치하는 리전을 선택합니다.
    
    [Region Table](https://www.notion.so/2f231434d9904e99b8ee78d8b347a706)
    

### 과제 4.2 백업, 데이터베이스 복원 및 애플리케이션 구성

- 💡4번.행 2-6에서 복사한 값을 **bash 터미널에 붙여넣으면** 이어서 수행하는 명령에서 사용할 수 있는 변수가 선언됩니다.
    
    ```bash
    h-4.2$ sudo cat /lab/db.config
    [DB]
    engine=mssql
    password=hh5mXQH-Db
    dbname=imagesdb
    dbhost=*imagesdb-instance.ca3mlzg7skse.us-west-2.rds.amazonaws.com*
    username=ap_service
    sh-4.2$ password=hh5mXQH-Db
    sh-4.2$ dbname=imagesdb
    sh-4.2$ dbhost=*imagesdb-instance.ca3mlzg7skse.us-west-2.rds.amazonaws.com*
    sh-4.2$ username=ap_service
    sh-4.2$
    sh-4.2$ echo $password
    hh5mXQH-Db
    sh-4.2$ echo $dbname
    imagesdb
    sh-4.2$ echo $dbhost
    imagesdb-instance.ca3mlzg7skse.us-west-2.rds.amazonaws.com
    sh-4.2$ echo $username
    ap_service
    ```

## 모듈 10: 데이터베이스 및 데이터 마이그레이션 서비스 이해

## 실습 4: 기존 데이터베이스를 Amazon Aurora로 마이그레이션


14.Windows PowerShell을 선택합니다.

<aside>
💡 powershell 스크립트 실행시에 반드시 Powershell(x86)이 아닌 **Powershell**을 선택하시기 바랍니다.

</aside>


# 3일 차

## 모듈11: 추가 마이그레이션 지원 옵션 이해
## 모듈 12: 애플리케이션 통합, 검증 및 전환
## 모듈 13: 애플리케이션 마이그레이션 현대화 및 최적화
## 실습 5: Amazon S3 및 Amazon ECS를 사용하여 애플리케이션 최적화
## 모듈 14: 운영 도구, 통합 테스트 및 자동화 이해
## 모듈 15: 마이그레이션 모범 사례
## 실습 6: 애플리케이션 배포 자동화







