### 10 부제
- 서울시는 6월 1일 부터 교통 혼잡을 막기 위해서 자동차 10부제를 시행한다. 자동차 10부제는 자동차 번호의 일의 자리 숫자와 날짜의 일의 자리 숫자가 일치하면 해당 자동차의 운행을 금지하는 것이다. 예를 들어 자동차 번호의 일의 자리 숫자가 7이면, 7일 , 17일, 27일에 운행하지 못한다. 또한, 자동차 번호의 일의 자리 숫자가 0이면 10일, 20일, 30일에 운행하지 못한다. 

- 여러분들은 일일 경찰관이 되어 10부제를 위반하는 자동차의 대수를 세는 봉사활동을 하려고 한다. 날짜의 일의 자리 숫자가 주어지고 7대의 자동차 번호의 끝 두 자리 수가 주어졌을 때, 위반하는 자동차의 대수를 출력하는 프로그램을 작성하라. 

### 풀이
```
function car(day, arr) {

  let answer=0

  for(let i = 0; i<arr[i]; i++) {
    if(arr[i] % 10 === day) answer++ 
    // arr의 값을 10나누었을 때 나머지 값이 day의 값이 면 answer++해라.
  }
  return answer 
}
const arr = [12,20,54,30,87,91,30]

car(0,arr)
```

### 풀이2
```
function car(day, arr) {

  let answer=0

  let arr1 =  arr.map((item) => item % 10)
  // arr의 나머지 값을 구하기 
  
  let arr2 = arr1.filter((item) => item === day)
  // arr1의 마지막 숫자와 day의 숫자와 같은 것을 구함.

  answer = arr2.length
  // arr2의 개수를 구함.
  return answer
  
}

const arr = [12,20,54,30,87,91,30]

car(0,arr)

```

## 풀이3
```
// 입력 숫자의 일의 자리 숫자와 날짜의 일의 자리 숫자 일치하는지 확인
function solution(num, arr) {
  let car = 0
  // 배열의 값을 루프를 돌려 일의 자리를 추출
    for(var i of arr){
     if (i % 10 === num){
        car++
      }
    }
  // 배열의 일의 자리의 숫자와 num의 숫자와 같은지 확인
  return car
}

let arr = [25,23,11,47,53,17,33]
solution(3,arr)

```