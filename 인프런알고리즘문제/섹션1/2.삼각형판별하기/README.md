## 삼각형판별하기

### 삼각형이 만들어지는 원리
- 선이 가장 긴 길이보다 짧은 두 길이의 합이 커야 삼각형이 만들어진다. 
- 1. 가장 긴 선의 길이를 먼저 구한 후
- 2. 세 길이를 모두 더한 총합의 값과 가장 긴 길이의 값을 뺀 후
- 3. 가장 긴 길이의 값이 더 큰지 비교하자.


### 내가 푼 풀이 방법
```
function solution(a, b, c) {
  let long = Math.max(a, b, c)
  let total = a + b + c
  let oper = total - long

   if (oper > long) {
     console.log('YES 😀')
    } else {
    console.log('NO 😂');
    }
 }

```

### 다른 풀이 방법
```
  function solution (a,b,c) {
    let answer="YES", max;
    let total = a+b+c
      if(a>b) max=a 
      else max = b
      if(c > max) max = c
      if(total - max <= max) answer='No'
      return answer   
  }

  console.log(solution(13,33,17))

```