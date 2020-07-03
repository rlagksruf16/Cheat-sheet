## C++ STL Sort2 CheetSheet [C++]

- STL 중 sort를 활용할 경우 3번째 인자에 다양한 사용자 함수 정의 가능
- 오름차순은 less<자료형>()
- 내림차순은 greater<자료형>()
- 사용자 정의 함수는 compare



#### sort() 사용자 정의 함수들

```c++
// 배열 정의
int arr[100];

// 첫번째 변수: 시작지점, 두번째 변수: 끝나는 지점
sort(arr, arr+100);  

// 오름차순, default
sort(arr, arr);
sort(arr, arr, less<자료형>());

// 내림차순
sort(arr, arr, greater<자료형>());

// 세번째 변수 사용 가능 -> 사용자 지정 함수 추가 가능
void compare(int a, int b) { // 내림차순으로 정의하기 위한 compare() 함수
  return a > b;
}

sort(arr, arr+ 100, compare);

```