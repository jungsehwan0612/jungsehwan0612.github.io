# GitHub 특강
## 1.  Git 기초
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
### 6. git remote add [GITHUB REPOSITORY ADDRESS]
현재 로컬 스토리지에 들어 있는 git 정보를 업로드 할 repository의 주소를 등록한다.
### 7. git push -u origin master
commit된 파일들을 로컬 스토리지에서 GitHub Repository로 복사한다.

## 2. 협업 툴로서의 GitHub
### 1.  GitHub에서 collaborator 추가
프로젝트 기획자(A)는 함께 일할 사람(B)의 GitHub ID를 등록한다.
B의 E-Mail로 초대 링크가 온다.
### 2. git clone [GITHUB REPOSITORY ADDRESS]
B는 작업하고 싶은 폴더에서 위 명렁어를 입력하여 GitHub Repository의 코드를 복제하여 가져온다.
### 3. git push -u origin master
B는 작업을 끝낸 후, repository로 작업 내용을 push한다.
### 4. git pull
A는 B의 수정 내용을 반영한 repository를 끌어와 A의 코드를 자동으로 수정한다.
### CONFLICT
만약 B가 작업하는 동안 A가 같이 작업하는 경우 conflict가 발생한다. 가능하면 이런 상황이 발생하지 않도록 A와 B의 충분한 소통이 필요하다!

## 3. Branch
### 1. "협업"? 한사람 밖에 일을 못한다?
위에서 살펴본대로, push/pull 만으로는 한 번에 repository를 한 명만 수정할 수 있다. 개인 프로젝트라면 상관 없지만, 협업으로서의 툴로 사용하기엔 제약 조건이 많다.
### 2. git branch [BRANCH NAME]
위에서 언급한 A와 B는 Branch라는 기능을 사용하면 동시에 작업이 가능하다.
A가 작업 중일 때, B가 git branch B라는 명령어를 입력하면 지금까지의 내용을 포함한 새로운 작업 분기점이 만들어진다. 이 분기점을 branch라 한다. (나무에서 갈라져 나온 나뭇가지 생각하면 된다.) 이 때, A가 작업하고 있던 기본 branch를 master brench라 한다.
## 3. git merge [BRANCH NAME]
A와 B가 모두 작업이 끝나면, 두 작업 내용을 합치는 작업이 필요하다. A가 master brench에서 git branch B라는 명령어를 입력하면 master brench와 B brench를 합치게 된다.
## CONFLICT
위에서 언급한 경우와 마찬가지로 conflict 상황이 당연히 발생한다. 이 때 A가 작업한 내용만 반영하는지, B가 작업한 내용만 반영하는지, 혹은 둘이 겹치지 않는다면 둘 다 반영하는지를 선택해주면 된다.
VS Code의 경우, 아주 편하게 클릭 한 번으로 세 가지 선택지 중 어떤 것을 선택할지 정할 수 있다.