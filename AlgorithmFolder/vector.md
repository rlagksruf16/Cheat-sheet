## C++ STL Vector, Pair CheetSheet [C++]



#### Vector

- 동적인 배열으로 자유롭게 추가, 삭제가 가능한 배열
- 크기, 메모리를 자동으로 설정하는 유동적인 배열



#### Vector 기본 함수들



```c++
//vector 정의
vector<자료형> [변수 이름] // vector<int> a;

// vector에 넣기 
a.push_back(x);

// vector에서 뒷부분 뽑아내기
a.pop_back();

// vector 앞부분 출력
a.front();

// vector 뒷부분 출력
a.back();

// vector 비어있는지 여부 확인 비어있으면 1 출력, 비어있지 않으면 0 출력
a.empty();

// vector 사이즈 출력
a.size();

// vector 모든 원소 삭제
a.clear();

```

