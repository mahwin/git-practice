.gitignore

모든 file.c

file.c

최상위 폴더의 file.c

/file.c

모든 .c 확장자 파일

\*.c

.c 확장자지만 무시하지 않을 파일

!not_ignore_this.c

logs란 이름의 파일 또는 폴더와 그 내용들

logs

logs란 이름의 폴더와 그 내용들

logs/

logs 폴더 바로 안의 debug.log와 .c 파일들

logs/debug.log
logs/\*.c

logs 폴더 바로 안, 또는 그 안의 다른 폴더(들) 안의 debug.log

logs/\*\*/debug.log

git reset
=> 커밋한 시점으로 돌아가 그 이후의 파일들은 다 지움.
git revert
=> 커밋한 내용과 반대의 행동을 함.

git reset --hard commit hash
=> 리셋됨.

git reset --hard
=> 마지막 커밋 상태로 되돌림.

git revert hash
=>hash 때 했던 커밋 내용을 반대로 실행함!!

만약에 되돌릴 파일에 특정한 내용이 커밋 후에 변경됐었다면 수정을 해줘야함

git revert --no-commit hash => revert를 시키는데 커밋은 하고 싶지 않을때.

Branch !

1.실제 배포되는 브랜치 2.테스트용 브랜치

git branch 브랜치 이름
git branch
=> 브랜치 이름이 나옴

브랜치 간의 이동
git switch 브랜치 이름

브랜치 삭제
git branch -d 브랜치 이름

브랜치 이름 변경
git branch -m 브랜치 이름 바꿀 이름

git log --all --decorate --oneline --graph

git log를 좀 더 시각적으로 잘 확인 가능.
소스 트리 사용하는 게 더 이쁨

병합
git merge
git rebase

rebase는 깔끔하게 브랜치가 통합됨
git merge는 브랜치는 그대로 두고 끝에서 새로운 커밋이 생기면서 병합됨!

=> 히스토리 깔끔? rebase고 merge는 브랜치 내용이 있었으면 좋겠으면!!

리베이스는 리베이스할 대상 브랜치로 가서
git swtich team-coatch
git rebase main
git merge team-coatch

충돌이 일어나면 ?

git merge할 때 충돌이 있을경우 >>>>>로 충돌 부분이 보임.
멈추고 싶으면 merge --abort

rebase는 커밋 하나하나 마다 다 차례 차례 해결해줘야함.

해결 후
git rebase --continue
를 반복해야함.

//////////////////////
github

git remote add origin
git push -u origin main
main 브랜치에서 origin 원격에다가 푸쉬하겠다.

git clone 주소 => .git 정보도 가져올 수 있음
