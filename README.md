git을 7년 넘게 사용하고 있지만, 체계적으로 찾아보지 않고 사용하고 있었다. 이번기회에 제대로 정리해보자.

# Git

Git !== Github  
Git: 분산 버전 관리 시스템. 인터넷이 없어도 사용 가능.  
Github: Git을 기반으로한웹 호스팅 서비스. Git 저장소를 온라인으로 공유할 수 있게
해주며, 협업 및 코드 공유, 이슈 추척, PR(MR), 코드 리뷰 등의 기능 제공.

요약하자면, Git은 소스 코드의 버전 관리를 위한 도구이며, GitHub는 Git을 사용하여
웹 상에서 협업 및 코드 공유를 쉽게 할 수 있는 플랫폼

## 명령어

[Git Docs](https://git-scm.com/docs)

### git init

- git init: 현재 디렉토리를 git 저장소로 만듦.

### git status

- git status: 변경 사항, 스테이징된 파일, 추적되지 않은 파일 등 작업 디렉터리의 상태를 표시.

### git add

- git add: 커밋을 준비하기 위해 스테이징 영역에 파일을 추가.
  - git add .: 현재 디렉토리의 모든 파일을 스테이징 영역에 추가.
  - git add -u: 현재 디렉토리의 변경된 파일을 스테이징 영역에 추가.
  - git add -p: 현재 디렉토리의 변경된 부분을 한줄씩 확인하며 스테이징 영역에 추가.

### git commit

- git commit: 스테이징 영역에 있는 파일들을 커밋.
  - git commit -m "message": 커밋 메시지를 함께 입력.
  - git commit -a: 변경된 파일을 자동으로 스테이징 영역에 추가하고 커밋. (단, 한번도 커밋되지 않은 파일은 스테이징 영역에 추가되지 않음.)
  - git commit -am "message": 변경된 파일을 자동으로 스테이징 영역에 추가하고 커밋 메시지를 함께 입력.
  - git commit --amend: 마지막 커밋을 수정.
  - 커밋 메세지는 과거시제(~했다)보다는 현재시제(~하다)을 사용하고 명령형으로 쓰는게 오피셜.

### git log

- git log: 커밋 로그 확인
  - git log --oneline: 커밋 로그를 한줄로 표시.

### git branch

- git branch: 브랜치 목록 확인.
  - git branch "name": 브랜치 생성
  - git branch -a: 로컬 브랜치와 원격 브랜치 목록 확인.
  - git branch -d "name": 브랜치 삭제. -D는 강제 삭제
  - git branch -m "name": 현재 브랜치 이름 변경.
    - git branch -m "old_name" "new_name": 다른 브랜치 or 현 브랜치에서 이름 변경 가능.

### git switch & checkout

- git switch "name": 브랜치 이동
  - git switch -c "name": 브랜치 생성 및 이동
- git checkout "name": 브랜치 이동
  - git checkout -b "name": 브랜치 생성 및 이동
  - git checkout

switch는 git 2.23에 새로 나왔는데, checkout과 간단히 비교하자면 git switch는 브랜치 간 전환에 보다 사용자 친화적이고 집중된 명령. 브랜치를 전환하거나 새 브랜치를 만들고 전환하는 것뿐.  
checkout은 브랜치를 전환하는 것 외에도 특정 커밋으로 전환하거나 작업 디렉토리의 변경 내용을 덮어쓰는 데에도 사용 가능.

## 자잘한 팁

- 윈도우에서 explorer로 폴더를 열었었는데, start로도 가능(이게 더 치기 쉽다.)
- git 기본 에디터를 vim에서 vscode로 변경: git config --global core.editor "code --wait"
- .gitignore 초기 설정에 도움을 주는 사이트: https://www.toptal.com/developers/gitignore/
