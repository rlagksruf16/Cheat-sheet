## C++ STL Vector CheetSheet [C++]

- 동적인 배열으로 자유롭게 추가, 삭제가 가능한 배열
- 크기, 메모리를 자동으로 설정하는 유동적인 배열
- vector 헤더 클래스에 포함 -> `#include <vector` 
- vector와 관련된 함수들은 아래의 기본 함수들 말고도 엄청 많다



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

// vector의 0번째 원소를 가리키는 iterator 리턴
a.begin();

//vector의 마지막 원소를 가리키는 iterator 리턴
a.end()l

// vector 비어있는지 여부 확인 비어있으면 1 출력, 비어있지 않으면 0 출력
a.empty();

// vector 사이즈 출력
a.size();

// vector 모든 원소 삭제
a.clear();

```



#### Vector와 알고있으면 좋은 예시



```c++

// <algorithm>의 reverse()를 활용하여 vector 의 원소들 순서 뒤집기
reverse(a.begin(), a.end());

// <algorithm>의 sort()를 이용하여 vector의 원소들을 오름차순으로 정렬하기
sort(a.begin(), a.end());

```
