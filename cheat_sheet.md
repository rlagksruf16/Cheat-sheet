# 내가 보기 위한 GIT 활용법

### git 이용해서 Push 하기
  
  
### Fork 한 repository 코드 최신화하기

- 오픈소스 프로젝트에 참여할때
- 개인이 아닌 많은 사람들과 협업할 때
  
####순서
1. 동기화할 새로운 레포지토리를 추가한다.
  
```bash
$ git remote add {repo 이름} { git 원본 repo url}
```
  
- repo 이름은 주로 `upstream`을 이용하지만 자기 원하는대로 해도 상관없다.
- git 원본 url은 처음에 fork 해온 원본 repository의 url를 의미하는 것이다.  
  
1.  추가한 새로운 레포가 추가되었는지 확인한다.

```bash
$ git remote -v
origin    