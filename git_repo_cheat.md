# 내가 보기 위한 GIT 활용법

## Fork 한 repository 코드 최신화하기  
  
  
#### 이용상황

  
- 오픈소스 프로젝트에 참여할때
- 개인이 아닌 많은 사람들과 협업할 때
  
  
  
#### 순서
1. 동기화할 새로운 레포지토리를 추가한다.
  
```bash
$ git remote add {repo 이름} { git 원본 repo url}
```
  
> repo 이름은 주로 `upstream`을 이용하지만 자기 원하는대로 해도 상관없다.
git 원본 url은 처음에 fork 해온 원본 repository의 url를 의미하는 것이다.  


  
2. 추가한 새로운 레포가 추가되었는지 확인한다.
  
```bash
$ git remote -v
origin https://github.com/내 이름/나의 fork.git (fetch)  
origin https://github.com/내 이름/나의 fork.git (push)  
upstream https://github.com/원본 제작자 이름/원본 repo.git (fetch)    
upstream https://github.com/원본 제작자 이름/원본 repo.git (push)  
```


> `git remote -v`를 이용하여 새로운 레포가 위와 같이 제대로 추가되었는지 확인할 수 있다.


  
3. 추가한 upstream repo로부터 최신 업데이트를 가져온다.

```bash
$ git fetch upstream
