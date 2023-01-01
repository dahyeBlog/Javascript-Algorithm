## 빅오표기법 개념 정리 
- 코드의 성능,효율성을 설명하는 방식 
- 여러가지 코드를 서로 비교하고 성능을 평가하는 방법 
- 숫자로 코드의 성능을 표기할 수 있다. 
- performance.now()메서드를 이용해서 코드실행 시간을 측정 할 수 있다. 
- 아래의 코드를 서로 비교해보면, 두번째 코드의 실행시간이 더 빠르다.
- 복잡도가 낮을 수록 좋은 알고리즘이라고 생각하면된다. 

## 시간 복잡도의 이해 

- 대략적으로 숫자를 세는 것에 붙인 공식적인 표현 
- 정식적으로 입력된 내용이 늘어날 수록 알고리즘에 실행 시간이 어떻게 변하는지 설명하는 공식적인 방식 
- 빅오는 어떤 함수의 입력값이 늘어나는 것과, 함수 실행 시간이 변하는 관계를 의미한다.


## 빅오표기법

```
  * n이란 입력되는 데이터를 의미
  - 선형 : f(n) = n  // n의 값이 커질 수록 실행 시간도 같이 늘어난다는 것임.
  - 제곱: f(n) = n² // 실행시간이 n의 제곱
  - 상수 : f(n) = 1 // n이 커져도 실행 시간에는 아무 영향도 받지 않기 때문에 항상 상수임.

```

### 빅오 표기법 예제

- O(1) : 스택의 Push, Pop
- O(log n) : 이진트리
- O(n) : for 문
- O(n log n) : 퀵 정렬(quick sort), 병합정렬(merge sort), 힙 정렬(heap Sort)
- O(n²): 이중 for 문, 삽입정렬(insertion sort), 거품정렬(bubble sort), 선택정렬(selection sort)
- O(2ⁿ) : 피보나치 수열




### 1 에서 N 숫자까지 더하기 알고리즘 첫번째방법

```
function add(params) {

  // 여러 연산들이 있고, 아래와 같은 코드에는 n이 커질 수록 실행 시간이 1:1 비율로 늘어나고 연산의 갯수는 n의 곱과 연결이 되어있다. 
  // O(n)이라 표현한다. 

    let total = 0
    for(let i = 1; i <= params ; i++) {
            total += i
    }

    console.log(total)
}

add(5)
```

### 1 에서 N 숫자까지 더하기 알고리즘 두번째방법

```
function addUpTo(n) {

  // 연산이 언제나 3개이다. 즉, 실행시간에 큰 변화가 없다는 뜻임.
  // O(1)이라 표현할 수 있다. 

    return n * (n + 1) / 2
}

console.log(addUpTo(6))
```

### O(n) 표기법의 예 - O(n) 표기법이 2개가 있어도 O(n) 라 표현한다. 

```
function countUpAndDown(n) {
    console.log('Going up!')

    //n이 늘어날 수록 루프안에 연산이 있다. 
    // O(n)이라 표기한다. n이 커질 수록 루프가 실행하는 횟수가 늘어나기 때문이다. 

    for(let i = 0; i < n ; i++) {
        console.log(i)
    }
    console.log('At the top!!\nGoing down...')

    //n이 늘어날 수록 루프안에 연산이 있다. 
    // O(n)이라 표기한다. n이 커질 수록 루프가 실행하는 횟수가 늘어나기 때문이다. 

    for(let j = n - 1; j >=0; j--) {
        console.log(j)
    }
    console.log('Back down, Bye!')
}


countUpAndDown(5)
```


## O(n²)의 표기법의 예 - n이 커질 수록 실행시간이 n²의 값으로 늘어난다는 것이다. 

```
function printAllParis(n) {
   
   // 첫번째 루프는 O(n)표기법을 사용한다. n이 커질수록 연산들이 n값만큼 늘어나기 때문이다. 

    for(var i = 0; i < n; i++) {

    // 안에 중첩 루프가 있다 똑같이 O(n)이다. 
    // 중첩되어 있기 때문에 O(2n)이 아니다. O(n)연산 안에 O(n)연산이 있으면, O(n²)이 된다. 

        for(var j = 0; j < n; j++) {
            console.log(i,j)
        }
    }
}

printAllParis(5)
```

## O(n) 빅오 표기법의 예 

```
function logAtLeast5(n) {
  
  // 5라는 숫자가 정해져 있지만, 다음에 n이 커질 수록 연산 갯수가 n에 비례해서 늘어나기 때문에 표기는 O(n)이라 한다. 
    for(var i = 1; i <= Math.max(5,n); i++) {
        console.log(i)
    }
}

logAtLeast5(10)
```


## O(1) 빅오 표기법의 예 

```
function logAtMost5(n) {
  
  // 5라는 숫자가 정해져 있기 때문에, 5보다 크면 무조건 더 작은 5를 선택할 것이기 때문이다. n이 1000이라도 루프가 5번만 반복된다. 

    for(var i = 1; i <= Math.min(5,n); i++) {
        console.log(i)
    }
}

logAtMost5(10)
```


## 공간 복잡도의 이해
- 입력이 커질 수록 알고리즘의 실행 속도가 바뀌는 것은 시간 복잡도의 설명이다. 
- 입력이 커질 수록 알고리즘이 얼마나 많은 공간을 차지하는지에 대한 것은 공간 복잡도의 설명이다. 
- n이 커질 수록 무한대 까지 가면서 입력자체가 커진다는 것이다. 
- booleans, numbers, undefined, null 값은 자바스크립트에서 모두 불변의 공간이다. 


## 빅오표기법 측정 참고 사이트
- https://rithmschool.github.io/function-timer-demo/