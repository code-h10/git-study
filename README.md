# Git Tool Tip

## 1. Stashing
현재 브랜치에서 작업하던 부분을 잠시 멈추고 다른작업을 위해 브랜치르 변경해야될 때 `git stash` 명령어를 사용하여 해결 할 수 있다.

1.1 stash 하기
```
$ git stash
```

1.2 stash 조회
```
$ git stash list
```

1.3 stash 적용
```
$ git stash apply : 최근 stash 순으로 working directory 적용
$ git stash apply --index : Staged 상태까지 적용
```

1.4 stash 삭ㅈ
```
$ git stash drop
```

## 2. 되돌리기

2.1 Commonit 메시지 수정 및 빼먹은 파일 추가하여 다시 Commit
아래의 명령어를 실행하면 첫번째 Commit 한 내용에 text.txt 파일을 추가하여 첫번째 Commit 을 덮어쓴다.
```
$ git commit -m "test"
$ git add test.txt
$ git commit --amend
```
