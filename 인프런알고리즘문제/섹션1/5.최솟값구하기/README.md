## 최솟값 구하기
- 7개의 수가 주어지면 그 숫자 중 가장 작은 수를 출력하는 프로그램을 작성하자.

## 풀이법1 - Math.min() 최솟값 구하기 메서드
```
function min(a,b,c,d,e,f,g) {
  let min = Math.min(a,b,c,d,e,f,g)
  return min
}

min(5,2,7,11,2,15,17)
```

## 풀이법2
```
function min(arr) {
  let answer, min=Number.MAX_SAFE_INTEGER; // 최대 안전 정수를 나타낸다.
  for(let i=1; i<arr.length; i++){
    if(arr[i]< min) min=arr[i]
  }
  answer=min
  return answer
}
let arr=[5, 7, 1, 3, 2, 9, 11];
min(arr)
```