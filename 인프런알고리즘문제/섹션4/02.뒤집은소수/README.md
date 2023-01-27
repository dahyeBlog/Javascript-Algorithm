## 자릿수의 합
- N개의 자연수가 입력되면 각 자연수를 뒤집은 후 그 뒤집은 수가 소수이면 그 소수를 출력하 는 프로그램을 작성하세요. 
- 예를 들어 32를 뒤집으면 23이고, 23은 소수이다. 그러면 23을 출 력한다. 단 910를 뒤집으면 19로 숫자화 해야한다.  
- 첫 자리부터의 연속된 0은 무시한다.

## 입력설명
- 첫 줄에 자연수의 개수 N(3<=N<=100)이 주어지고, 그 다음 줄에 N개의 자연수가 주어진다. 각 자연수의 크기는 100,000를 넘지 않는다.

## 출력설명
- 첫 줄에 뒤집은 소수를 출력합니다. 출력순서는 입력된 순서대로 출력합니다.

##  입력예제 1
- 9
- 32 55 62 20 250 370 200 30 100

##  출력예제 1 
- 23 2 73 2 3


## 풀이법
```
function isPrime(num) {
 if(num === 1) { //음수와 1은 소수가 아니다.소수는 1보다 큰 정수임.1보다 작으면 false임.
  return false
 } else {
  for(let i = 2;i<=parseInt(Math.sqrt(num)); i++){ //2는 짝수 중 유일한 소수이다.
   if(num % i === 0){ // num이 다른 수로 나눠 떨어진다면 소수가 아니다.
    return false
   }
  }
 }
  return true
}



function solution(arr) {
 let answer = []
 for(let x of arr){
  let res = (Number(x.toString().split("").reverse().join('')))
  if(isPrime(res)) {
   answer.push(res)
  }
 }
 return answer
}

const arr = [32,55,62,20,250,370,200,30,100]

solution(arr)
```
