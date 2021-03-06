# Using stack in C++  

C++ 를 사용하다 보면 데이터를 규칙있게 저장해야 할 때가 있다.  
[verifyBraces.md](https://github.com/denmark111/TIL/blob/master/Codewars/verifyBraces.md) 가 대표적인 예시이다.  
이 문제에서는 열림기호화 닫힘기호가 올바르게 짝지어져야 하는데 이러한 경우에 스택 구조를 사용하면 수월하게 해결가능하다.  

## How does it works?  
기본적인 동작은 LIFO 스택구조와 동일하다.  
먼저 삽입된 컨테이너가 가장 밑의 공간에 저장되는 구조이다.  
~*물론 직접 클래스를 제작하여 사용 할 수도 있지만 귀찮으므로*~

스택은 STL 의 `Containers adaptors` 에 속한다.  
이는 스택이 어떤 정해진 자료형을 가지는것이 아닌, 입력되는 자료를  
하나의 컨테이너로 보고 다룬다는 뜻이다.  
따라서 스택에는 다양한 자료형을 입력할 수 있다.  

예를 들면 같은 STL에 속하는 벡터 배열을 스택에 삽입 할 수도 있고 맵을 삽입 할 수도 있다.  

STL의 여러 종류는 별도의 문서에서 기술한다.  

## How to use it?  
스택을 사용하는 방법은 여타 STL 컨테이너와 다를바가 없다.  
``` C++  
#include <stack>

stack<int> st;  // 정수형의 데이터를 가지는 스택을 선언한다.  
```  
위와 같은 형식으로 선언하며 일반적인 스택 조작 함수들을 가지고 있다.  

``` C++
st.push(10);
st.pop();
```
