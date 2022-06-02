### 1. Tag 조회

1.1 Tag 기본 조회
```
$ git tag
```

1.2 Tag 검색패턴
```
$ git tag -l "v1.8.5*"
```

### 2. Tag 붙이기

2.1 Annotted Tag
git 데이터베이스에 태그를 만든 사람의 이름, 이메일과 태그를 만든 날짜, 그리고 태그 메시지를 저장한다.

```
$ git tag -a v1.4 -m "my version 1.4"
$ git tag
v0.1
v1.3
v1.4
```

2.2 LightWeight Tag
파일에 커밋 체크섬을 저장하는 것뿐이다.
```
$ git tag v1.4-lw
$ git tag
v0.1
v1.3
v1.4
v1.4-lw
v1.5
```

### 3. 나중ㅇ Tag 하기
커밋을 태그하지 못했다고해도 명령어 option 중 `-a` 를 사용하여 Tag 를 붙일 수 있다.
```
$ git tag -a v1.2 0fceb02
v0.1
v1.2
v1.3
v1.4
v1.4-lw
v1.5
```


### 4. Tag 공유
Tag 를 만들었으면 서버에 별도로 push 해야한다.
```
$ git push main v1.5
```
태그를 여러개 push 하려면 아래와 같이 하면된다.
```
$ git push main --tags
```
