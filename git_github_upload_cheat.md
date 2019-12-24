# 내가 보기 위한 GIT & GITHUB Upload 활용법

### GIT을 이용해서 GITHUB에 업로드 하는 법

### 이용상황

- local 에서 작업한 프로젝트 업로드하기



### 순서 (초기)

**0. git 버전 확인**

```bash
$ git --version
git version 2.22.0.windows.1
``` 

> 'git --version' 를 입력하여 git이 컴퓨터에 제대로 설치되어 있는지 확인한다.


**1. git init 명령어**

```bash
$ git init
Initialized empty Git repository in C:/Users/솰랴솰랴
``` 

> 'git init' 명령어는 git 저장소를 초기화 해주거나 git 저장소를 만들어주는 역할을 한다. 어떠한 프로젝트를 git으로 관리하고 싶으면 git init 명령어를 실행하면 된다.


**쉬어가는 타임 git status 명령어**

```bash
$ git status
On branch master
No commits yet

``` 
> 'git status' 명령어는 저장소의 상태를 체크하고 변경사항이 어떤 것인지 확인해주는 명령어이다. git add 또는 git commit 명령어 전 또는 후에 이용가능하다

**2. git add .**

```bash
$ git add . & git add -A
``` 

> 'git add' 명령어는 작업공간인 working directory에서 staging area로 보내는 명령어이다. 프로젝트 진행 중에 특정파일을 수정하였거나 생성하여 그 부분을 업로드하고 싶으면 git add . 또는 git add -A 부터 시작하면 된다.


**3. git commit -m "commit 메세지"**

```bash
$ git commmit -m "first commit ~~~"
1 file changed, 12 insertions(+)
create mode 100313132 1.html
``` 

> 'git commit -m " " ' 명령어는 staging area에서 local repo로 저장해주는 명령어이다. 이전 add 했던 파일들을 저장소에 저장해준다고 생각하면 쉽다! commit 은 기억하다 어떤 행위를 하다 라는 뜻으로 쓰이고 commit 은 add 와는 다르게 수정사항을 입력할 수 있다.

> commit 메세지는 누구나 볼 수 있기에 직관적이고 알아보기 쉽게 작성하는 것을 권장!


**4. git repo와 github 연동**

```bash
$ git remote add origin http://깃허브 주소.git
```

> git commit 까지는 git의 로컬 저장소에만 해당하는 부분이다. 로컬 저장소와 온라인 저장소인 github를 연결해야겠죠? 그게 바로 'git remote add' 명령어 입니다.


**5. git push 명령어**

```bash
$ git push -u origin master

```
> 로컬 저장소와 github를 연결까지 했으면 로컬 저장소에 있는 자료들을 github에 업로드 해야겠죠? 'git push' 명령어는 연결해주는 명령어입니다. 로컬 저장소에서 github로 밀어버린다고 생각하면 쉽게 외워져요!


### 참조

[근둥이의 블로그](https://codevkr.tistory.com/46)  