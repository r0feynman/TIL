#Git

##1.Shell cmd

- ls : list segment
- ls -a : 숨긴파일 / all
- ls -l : line by line 상세정보
- ls -al
- ls .bin/

###이동

- cd .. : 상위 디렉토리
- cd . : 현재 위치

###생성

- mkdir : make directory
- touch : 파일 생성

###파일 이동

- mv <원본> <대상> 
- rename도 mv 명령어로 가능
- * : wild card

###복사
- cp <파일명> <위치 or 새파일명>

###삭제

- rm <파일명>
- rm -r <디렉토리명>
- rm -rf : force

##2. Vim cmd

모드 기반
- insert mode : i
- normal mode : esc

:wq
:q!

##3.Git cmd

blob : object
tree : blob이나 subtree의 메타데이터(디렉토리 위치, 속성, 이름 등)
commit : commit 순간의 스냅샷

git status

git add
git commit
git switch

git push
git pull

HEAD : latest!

##4.Conventional Commits
1. commit의 제목은 문장형이 아닌 구나 절로 ! 짧고 간결하게!
2. 첫 문자는 대문자로!
3. prefix 꼭 달기!
    - feat : 기능 개발 관련
    - buil : 빌드 작업
    - fix : 오류 개선 혹은 버그 패치
    - docs
    - test
    - conf : 환경설정
    - ci
    - chore : 패키지 매니저, 스크립트
    - style : 코드 포매팅

e.g. 
feat : Create Add Function

##5. Branch

git branch
git branch -a
git branch -r

git branch <name>
git switch <name>

branch는 공간의 개념
commit은 시간의 개념

git remote
git remote -v

git merge <name>
git branch -D <name>

