<img src="https://online.spartacodingclub.kr/assets/icons/logo-web.svg" height="100"/>

# 스파르타 코딩클럽 Git 강의 회고 

> 김치 레시피를 예로 한 git 강의 자료 입니다.
- Github url: https://github.com/9yuhyeon/9yuhyeon.github.io
- 사이트에 대한 1-2단락 설명

## 1주차
- 버전관리 : git commit을 통해 프로젝트 상태가 업데이트 되는 과정을 기록을 남기는 것
- git 초기화(git initialize) : 프로젝트 directory를 git이 관리할 수 있도록 설정하는 것
- commit : 프로젝트 작업 내용을 메시지와 함께 중간 저장하는 개념(commit 메시지는 누가, 언제, 무엇을 작업했는지 잘 표현하기!)
- add(staging) : commit을 하기 위해 작업 파일을 stage로 추가하는 것
- repository(repo): 내 pc에 저장되어 있는 Git 저장소를 로컬 repo라 하고, Github와 같이 다른 곳에서 접속할 수 있는 저장소는 원격 repo라고 한다.
- tracking(추적) : 로컬 repo branch와 원격 repo branch를 연결하는 것
- push : 로컬 repo branch기준으로 원격 repo branch에 새로운 commit들을 반영하는 것
- pull : 로컬 repo branch 기준 원격 repo branch에서 새로운 commit들을 가져와 로컬 repo branch에 반영하는 것
- clone : 원격 repo를 내 pc에 가져와 초기 repo 셋팅하는 것
> 충돌을 최소화 할 수 있는 방법
 - 원격 repo에 변경사항이 생겼을 경우 원격 repo에서 먼저 pull 로컬 repo에서 작업하기!
1. 로컬 repo에 원격 repo 작업내역 가져오기(pull)
2. 로컬 repo의 작업 내용을 commit하기
3. 원격 repo에 로컬 repo commit을 반영하기(push)
![image](https://user-images.githubusercontent.com/112394164/189557511-c1e5a576-1d8d-4a50-a988-ee52740ab0a5.png)

## 2주차
> 협업하는 과정
 
 Issue 👉 Branch 👉 Pull request 👉 merge
 - Issue : 프로젝트 진행 시 담당 프로젝트 할당하는 것
 - Branch : 할당 받은 프로젝트를 main 프로젝트와 분리하여 별도로 작업할 수 있는 공간(main 프로젝트 및 다른 branch에 반영되지 않음)
 - Pull request : 나의 Branch에서 commit한 history를 main이나 다른 branch에 반영하기 전 의견을 수렴하는 과정
 - Merge : PR에서 승인 한 경우 main 혹은 다른 branch에 나의 branch를 합치는 것 
 - Merge conflict : merge 하는 과정에서 충돌이 일어난 경우(주로 같은 파일을 수정할 때 발생)
 
 ✔️push와 pull은 tracking되고 있는 branch를 기준으로 commit을 반영하기 때문에 브랜치 checkout을 잘 확인하자!!!
 
 ## 3주차
 > Commit 관리하기
 
 🤦‍♂️작업하다가 commit 메시지에 오타 or 파일 add들 놓친 경우 되돌리는 방법들
 - amend : 가장 최신의 commit을 수정하는 방법(파일 상태로 들어가 우츨 하단에서 마지막 커밋 수정 클릭 후 다시 커밋)
 - stash : 임시저장 기능으로 커밋하지 않은 내역을 스태시 보관함으로 이동(커밋이 없었던 파일은 추적하지 않아 따로 stash하지 않아도 됨)
 - revert : 선택한 commit을 되돌리면서 commit을 다시 남기는 것(가장 최신 혹은 이전 commit도 가능)
 - reset : 선택한 commit으로 되돌리지만 soft, mixed, hard 방식 중 선택하여 되돌림
 1. soft : 선택한 커밋 까지의 커밋은 되돌리고 파일 작업 내역은 보존해서 파일 변경사항으로 남음
(커밋 메시지는 사라지지만 파일의 변경사항은 그대로 남아있고 add(staging)된 상태로 되돌아감)
 2. mixed : 선택한 커밋 까지의 커밋은 되돌리고 파일 작업 내역은 보존해서 파일 변경사항으로 남음
(soft와 동일하게 커밋 메시지는 날라가지만 파일의 변경사항은 선택한 커밋 이전까지 모두 남아있으며 add(staging 되지 않은 상태에서 남음)  
 3. 🚨hard🚨 : 선택한 커밋 이후의 커밋들을 싹 날려버림 (수정 불가! 이거슨 되돌릴 수 없는 선택...☆)
 
 🔔 커밋 되돌리는 것은 내 Issue의 branch에서만 사용하자!!!
 
- commit 메시지 컨벤션 : 프로젝트를 함께 진행하는 조직 내 메시지를 작성하는 합의된 규칙

💡 좋은 commit 메시지를 작성하면 어떤 작업을 했는지 history만 보고 알 수도 있고, 버그를 찾기 수월하며 다른 사람이 코드를 리뷰하기 편한다.
- gitignore : 공개되면 안되는 파일들은 공개된 repo에 올라가면 안되기 때문에 .gitignore을 통해 파일을 git에서 숨김 처리 할 수 있다.
- README.md : 프로젝트를 잘 이해할 수 있도록 하는 소개글(한 눈에 알아볼 수 있게 잘 작성하자!)
 



