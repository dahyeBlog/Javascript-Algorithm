## 가장 긴 문자열
- N개의 문자열이 입력되면 그 중 가장 긴 문자열을 출력하는 프로그램을 작성하세요.

##  입력예제 1
```
teacher
time
student
beautiful 
good

```

##  출력예제 1 
- beautiful

## 내가 푼 방법
```
function solution(str) {
  // 배열을 받아와 반복문을 돌린다.
  // 가장 긴 숫자를 비교 후 maxNum에 가장 긴 숫자를 할당한다.
   let maxNum = 0
    let answer = []
   for(let x of str){
     if(x.length > maxNum){
         maxNum = x.length
         answer= x
     } 
      
   }
    return answer
}

let str = ['teacher','time','student','beautiful','good']

solution(str)
```