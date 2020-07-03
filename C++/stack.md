## C++ STL Stack CheetSheet [C++]

- 스택은 탑을 쌓아간다는 의미
- LIFO(Last in First out)



#### Stack 기본 함수들

```c++
// 스택 정의
stack <자료형> s;

// 스택에 집어 넣기
s.push(x);

// 스택의 가장 윗 부분 뽑아내기
s.pop();

// 스택의 가장 윗 부분 확인하기
s.top();

// 스택이 비어있는지 확인 ( 비어있으면 1, 남아있으면 0의 값 리턴)
s.empty(); 

// 스택의 사이즈 반환
s.size();

```



