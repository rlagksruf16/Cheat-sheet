## C++ STL Pair CheetSheet [C++]

- Pair 클래스는 어떠한 두개의 객체를 하나로 묶어서 하나의 쌍으로 이용할 수 있게 해주는 클래스
- vector, queue, stack 등에서 2개의 원소들을 묶어줄 때 사용
- sort 함수로 정렬 가능 -> 첫번째 원소들 부터 정렬 후 두번째 원소들 정렬 ( sort의 세 번째 파라미터로 조정 가능)



#### Pair 기본 함수들

```c++
//Pair 정의
pair<type, type> p;

// pair의 첫 번째 원소에 접근
p.first;

// pair의 두 번째 원소 접근
p.second;

// 두개의 원소들을 묶어서 pair에 저장
make_pair(a1, a2);

// vector 와 pair 를 이용한 정의
vector<pair<int, int>> v;
```

