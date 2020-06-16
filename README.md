# CodeBot Guide
## Overview
> CodeBot 시스템은 개발자와 리뷰어간의 원활한 코드리뷰 수행을 지원하기 위해 다양한 자동화 기능을 제공하는 코드리뷰 지원 서비스입니다.

CodeBot은 GitHub으로부터 PR(Pull Request) 이벤트가 발생하면, 변경된 소스를 기준으로 다양한 정적 분석(Static Analyst)을 수행하고, 리뷰어를 자동 지정하는 등의 코드리뷰 활동에 필요한 다양한 서비스를 제공합니다.

제공되는 서비스는 다음과 같습니다.
* 잠재결함 분석
  * 잠재결함 자동 수정(Autofix) 기능
* CAM(Code Archtecture Metric) 분석
* Build 테스트 결과
* Unit 테스트 결과
* 리뷰어 자동 지정
* 오탈자 분석 기능

지원되는 언어는 다음과 같습니다.
* Java (Maven / Gradle / Ant)
* JavaScript
* Python

## Usage
### Codebot 서비스 사용 준비
#### 서비스 신청
CodeBot 사용을 위해서는 GitHub에 대한 접근 권한이 필요합니다. 이를 위해 GitHub에서 Personal Access Token을 생성한 후 CodeBot에 등록이 필요합니다.
#### GitHub Personal access token 생성
1. 오른쪽 상단의 프로필 사진을 클릭한 다음 Settings를 클릭합니다.
2. 왼쪽 사이드 바에서 Developer settings를 클릭합니다.
3. 왼쪽 사이드 바에서 Personal access tokens를 클릭합니다.
4. 오른쪽의 Generate new token을 클릭합니다.
5. Token의 이름을 입력합니다.
6. Token에 부여하려는 권한을 선택합니다. CodeBot 사용을 위해서 다음의 권한이 필요합니다.
   * repo (Full control of private repositories)
   * admin:org (Full control of orgs and teams, read and write org projects)
   * amdin:repo_hook (Full control of reporitory hooks)
7. Generate token을 클릭합니다.
8. :clipboard:버튼을 클릭하아여 클립보드에 복사합니다. 보안상의 이유로, 페이지를 떠나면 Token을 다시 볼 수 없습니다.

[GitHub Personal Access Token 생성 가이드](#github-personal-access-token-생성)

