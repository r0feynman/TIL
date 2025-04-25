# Git for Collaborative Work

## 1. Merge Conflict

- git은 라인 단위로 추적

## 2. Solve Merge Conflict
#### 1. merge 상황에서 해결
#### 해결법
1. 충돌된 브랜치 중 하나를 없애기
2. 둘 다 살리기
3. 중재하기
====, <<<<, >>>>는 꼭 삭제
#### 2. rebase의 방법으로 해결
- base를 다시 설정하는 아이디어 
- (빨간색 입장에서 베이즈를 검정색->파란색)
![[Pasted image 20250423110939.png]]

- git rebase main (hashtag branch 위에서)
#### rebase에서의 confilct 발생시
git rebase --continue
## commit의 종류
1. 일반 commit
2. merge commit

# Git Branching Strategy
## 1. Branch models

- git flow
- github flow
- gitlab flow

### git flow
main -> dev -> feature
![[Pasted image 20250423124501.png]]

### github flow
main -> feature -> pull request -> main
![[Pasted image 20250423124644.png]]
- Issues
	- git push -u origin <branch name> : upstream local의 branch를 origin에 첫 push할때
	- branch 단위 push
	- close : 이슈를 닫을때
	- fix : 이슈의 문제상황이 해당작업으로 수정되었을때
	- resolve : 이슈가 PR로 해결되었을 때
	- 각 단어는 현재형 복수형 과거형으로 표현 가능함

	- Issue Labels
- Pull requests
- sync up
	- ~~git pull origin main~~
	- git fetch origin main
	- git merge FETCH HEAD
### gitlab flow
배포 과정이 더 세심해짐
![[Pasted image 20250423124734.png]]


# Trouble shooting

## 1. Stash
작업중인 변경사항 잠시 미뤄두기
- git stash
- git stash save {message}

조회
- git stash list

복원
- git stash pop / git stash pop {index}
- git stash apply

삭제
- git stash drop {index}

## 2. Undo
working directory에서 변경사항 취소하기
- git restore {file name} : 최근 커밋으로 되돌리기
## 3. Unstaging
on stage area
- git add 실행 직후
- git reset HEAD fibo.py

- git restore --staged
## 4. Edit commit message
- git commit --amend : 직전 커밋 메세지 수정
- git rebase -i <commit>
- git rebase --continue 
- rebase 취소 : git rebase --abort

## 5. Reset commit
없었던 일로 만들기
- git reset --hard HEAD
- git push -f origin

## 6. Revert commit
특정시점으로 되돌리기
- git revert --no-commit HEAD~{nums of commit}..
- git commit

- git revert --abort
