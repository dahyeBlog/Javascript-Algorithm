### 일곱난쟁이
- 왕비를 피해 일곱 난쟁이들과 함께 평화롭게 생활하고 있던 백설공주에게 위기가 찾아왔다. 일과를 마치고 돌아온 난쟁이가 일곱 명이 아닌 아홉 명이었던 것이다. 아홉 명의 난쟁이는 모두 자신이 "백설 공주와 일곱 난쟁이"의 주인공이라고 주장했다. 뛰어난 수학적 직관력을 가지고 있던 백설공주는, 다행스럽게도 일곱 난쟁이의 키의 합이 100이 됨을 기억해 냈다. 아홉 난쟁이의 키가 주어졌을 때, 백설공주를 도와 일곱 난쟁이를 찾는 프로그램을 작성하시오.

### reduce() 메서드
- reduce() 메서드는 배열의 각 요소에 대해 주어진 리듀서 (reducer) 함수를 실행하고, 하나의 결과값을 반환한다.


### splice() 메서드
- splice() 메서드는 배열의 기존 요소를 삭제 또는 교체하거나 새 요소를 추가하여 배열의 내용을 변경합니다.


### 풀이
```
function nan(arr) {
  let answer = arr
  let sum = answer.reduce((a,b) => a+b,0)
  // reduce 함수로 arr의 전체 합을 구하기
  
  for(let i  = 0 ; i < arr.length; i++) {
     for(let j = 1; j<arr.length; j++){
      
       if(sum - (arr[i]+ arr[j]) === 100 ) {
          answer.splice(i,1)
           // splice함수로 i번째의 숫자 한개를 삭제해라.
          answer.splice(j,1)
           // splice함수로 j번째의 숫자 한개를 삭제해라.
       }
      

    }   
 
  }
   return answer
  

}

const arr = [20,7,23,19,10,15,25,8,13]
nan(arr)
```