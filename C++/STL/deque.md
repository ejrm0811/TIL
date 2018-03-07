# Using deque in C++  

간혹 C++를 사용하다보면 양쪽에서 접근가능한 리스트가 필요할 때가 있다.  
이 문서에서는 위와 같은 상황에서 사용할 수 있는 `deque (double ended queue)` 를 알아본다.  

제작의 편의성을 위해 아래에서는 `deque` 를 `더블큐` 라 부른다.  

### How does it works?  
더블큐는 그 시작과 끝에서 모두 접근이 가능한 자료형이다.  
각각의 끝단의 원소를 가리키는 포인터가 존재하며 이 포인터는 반드시 유효한 원소를 가리킨다.  

양쪽 끝에서 접근이 이루어지므로 당연히 벡터 컨테이너와는 다르게 원소가 삽입되는 순서대로 저장되지는 않는다.  
또한 벡터 컨테이너의 경우 임의의 적당한 저장공간이 자동으로 할당되고 만약 그 공간을 초과한다면  기존의 모든 원소를 더 넓은 새로운 저장공간으로 이동하는데에 비해 더블큐는 새로운 값을 새로운 메모리 공간에 할당하므로 비용이 상대적으로 적다.  

### How to use it?  
여타 STL과 같이 더블큐도 해더를 선언하는것으로 시작한다.  
``` C++
#include <deque>

using namespace std;

deque<int> dq;
```
위와 같은 코드는 정수를 원소로 갖는 더블큐를 선언한다.  