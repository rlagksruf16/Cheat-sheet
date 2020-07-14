#### std::find 함수

- C++ algorithm 헤더파일 안에 존재
- 배열에 활용해도 되고 vector에 활용해도 된다
- 특정 배열 안에 있는지 없는지 여부를 확인해주는 함수
- True or False 반환


#### fint() 함수

```c++
// 방법 1

// vector 정의
vector<int> v;

if ( std::find(v.begin(), v.end(), item) != v.end() )
    this(); // 존재하면
else
    that(); // 존재하지 않는 다면

// 방법 2

// 배열 정의
int a[4] = {10, 20, 30, 40};

p = std::find(a, a + 4, 30);

if (p != a + 4)
    std::cout << "Element found in a: " << *p << '\n';
else
    std::cout << "Element not found in a\n";

```

