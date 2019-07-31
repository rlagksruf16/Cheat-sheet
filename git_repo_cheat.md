# 내가 보기 위한 GIT 활용법

### Fork 한 repository 코드 최신화하기  
  
#### 이용상황

- 오픈소스 프로젝트에 참여할때
- 개인이 아닌 많은 사람들과 협업할 때  
  
  
  
#### 순서(초기)

**1. 동기화할 새로운 레포지토리를 추가한다.**
  
```bash
$ git remote add {repo 이름} { git 원본 repo url}
```  

> repo 이름은 주로 `upstream`을 이용하지만 자기 원하는대로 해도 상관없다.
git 원본 url은 처음에 fork 해온 원본 repository의 url를 의미하는 것이다.  



**2. 추가한 새로운 레포가 추가되었는지 확인한다.**
  
```bash
$ git remote -v
origin https://github.com/내 이름/나의 fork.git (fetch)  
origin https://github.com/내 이름/나의 fork.git (push)  
upstream https://github.com/원본 제작자 이름/원본 repo.git (fetch)    
upstream https://github.com/원본 제작자 이름/원본 repo.git (push)  
```  


> `git remote -v`를 이용하여 새로운 레포가 위와 같이 제대로 추가되었는지 확인할 수 있다.    



**3. 추가한 upstream repo로부터 최신 업데이트를 가져온다.**  
  
```bash
$ git fetch upstream
remote: Counting objects: 56, done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 76 (delta 35), reused 35 (delta 9)
Unpacking objects: 100% (61/61), done.
From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
 * [new branch]      master     -> upstream/master
```  

> `git fetch upstream` 을 통해서 새로 생성한 upstream repo에 최신 업데이트를 저장하는 것이다.  



**4. upstream repo 에서 나의 local로 merge 한다.**  
  
```bash
$ git merge upstream/master
Updating a422352..5fdff0f
Fast-forward
 README                    |    9 -------
 README.md                 |    7 ++++++
 2 files changed, 7 insertions(+), 9 deletions(-)
 delete mode 100644 README
 create mode 100644 README.md
```  

> 이제 나의 local repo에 merge가 되었다.  


  
**5. 마지막으로 remote 에도 적용해준다.**  
  
``` bash
$ git push -u origin master
```  
> 지금까지 진행 한 것은 local repo에 일어난 것이므로 push를 통해 remote repo에도 적용시켜 준다.


#### 지속적으로 할 경우(처음이 아닌 경우)  
만약 지속적으로 최신화를 해야 하는 경우 초기에 위와 같은 순서대로 설정을 해주고 **3 ~ 5번**을 지속적으로 하여 계속해서 새로운 repo를 만드는 것이 아니라 upstream를 업데이트 시켜주는 식으로 진행한다.  



## 부록(부가적인 명령어)  
  
#### 리모트 저장소 이름 변경
  
```bash
git remote rename {바꿀 repo 이름} {변경될 repo 이름}
```
  
> `git remote rename {기존 repo 이름} {원하는 repo 이름}` 을 통해서 이름을 변경할 수 있다. 주로 이름은 `upstream` 을 이용한다.
  
  
#### 리모트 저장소 삭제
  
```bash
git remote rm {repo 이름}
```
  
> `git remote rm {repo 이름}` 을 통해서 리모트 저장소를 삭제할 수 있다.

#### 참조

[mylko72님의 블로그](https://mylko72.gitbooks.io/git/content/remote/remove.html)  

[GIT 공식 문서](https://git-scm.com/book/ko/v1/%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0)

[https://help.github.com/en/articles/syncing-a-fork](https://help.github.com/en/articles/syncing-a-fork)