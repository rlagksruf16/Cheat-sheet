#### C++ STL Sort CheetSheet [C++]

- C++ algorithm 헤더파일 안에 존재
- 기본적으로 퀵 정렬을 기반으로 구성된 것이기 때문에 시간복잡도는 O(nlogn)
- 오름차순이 default



#### sort() 기본 함수들

```c++
// 배열 정의
int arr[100];

// 첫번째 변수: 시작지점, 두번째 변수: 끝나는 지점
sort(arr,arr+100);  

// 세번째 변수 사용 가능 -> 사용자 지정 함수 추가 가능
void compare(int a, int b) { // 내림차순으로 정의하기 위한 compare() 함수
  return a > b;
}

sort(arr, arr+ 100, compare);

// 객체로 지정한 것들을 세번째 변수 이용으로 정렬 가능

```

