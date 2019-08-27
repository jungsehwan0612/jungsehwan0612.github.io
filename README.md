# GitHub 특강
## 1.  Git 사용법
### 1. Git을 활용하고 싶은 Directory를 Git Bash에서 접근
cd: change directory
mkdir: make directory
ls: 해당 디렉토리에 들어 있는 파일 및 디렉토리를 리스트로 출력
### 2. git init
### 3. git status
현재 git staging area의 변경 사항, 확인되지 않은 파일 등을 표시해준다.
### 4. git add [FILENAME]
git staging area에 해당 파일을 추가한다.
### 5. git commit -m "[COMMIT MESSAGE]"
staging area에 들어 있는 파일(=변경 사항)을 commit 한다.
###6. git push -u origin master
commit된 파일들을 로컬 스토리지에서 GitHub Repository로 복사한다.