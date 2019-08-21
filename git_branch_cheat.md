# 내가 보기 위한 GIT Branch 활용법

### 나만의 Branch를 생성하여 작업하기  
  
#### 이용상황

- 혼자 작업하는데 확신이 들지 않을 때
- 오픈소스 프로젝트에 참여할때
- 다른 사람들과 프로젝트성으로 협업할 때

**1. 브랜치 생성 및 브랜치 확인**

```bash
$ git branch { 브랜치 이름 } //브랜치 생성
$ git branch //브랜치 확인
```

> `git branch`를 입력하면 현재 branch를 다 보여준다

  
**2. 브랜치 전환**

```bash
$ git checkout { 브랜치 이름 }
```
  
> `git checkout -b { 브랜치 이름 }` 을 이용하면 브랜치 생성과 체크아웃을 동시에 실행할 수 있다.

  
**3. 브랜치 삭제**

```bash
$ git branch -d { 브랜치 이름 }
```

  
**4. 브랜치 병합하기**

```bash
$ git merge { commit 한 브랜치 }
```

> master branch 이외의 다른 branch에 add 후 commit 한 다음, master branch로 checkout 해서(head에 있도록 해준 다음) `git merge 다른 branch` 를 입력해주면 master branch와 다른 branch와 같아 진다.



### 참조

[누구나 쉽게 이해할 수 있는 Git 입문](https://backlog.com/git-tutorial/kr/stepup/stepup2_8.html)