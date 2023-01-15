### 문자찾기
- 한 개의 문자열을 입력받고, 특정 문자를 입력받아 해당 특정문자가 입력받은 문자열에 몇 개 존재하는지 알아내는 프로그램을 작성하세요. 문자열의 길이는 100을 넘지 않습니다.

### 문제 풀이 1
```
function solution(str, a) {
    let answer = 0
    // str 의 문자열 중, a의 숫자가 몇개가 존재하는지 확인하라.
    // 루프를 돌려 문자열을 하나씩 확인하라.
    for(let x of str){
      if(x.includes(a)){
          answer++
      }
    }
    return answer
}

const str = 'COMPUTERPROGRAMMING'
solution(str, 'R')
```

### 문제 풀이 2
```
function solution(str, a) {
    let answer = str.split(a).length;
    // a를 기준으로 문자열을 나눈다. 
    return answer-1
    }

const str = 'COMPUTERPROGRAMMING'
solution(str, 'R')
```

