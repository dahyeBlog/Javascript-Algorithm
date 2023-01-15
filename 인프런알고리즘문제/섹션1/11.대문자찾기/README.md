## 대문자 찾기
- 한 개의 문자열을 입력받아 해당 문자열에 알파벳 대문자가 몇 개 있는지 알아내는 프로그램을 작성하라.

### 풀이 
```
function solution(str) {
    let answer = 0
    const regex = /^[A-Z]/g;
     
    // str의 문자열을 루프를 돌려 하나씩 확인하라.
    for(let x of str){
        if(regex.test(x)) answer++
    }
    return answer
 // 만약 str의 값에 대문자가 있다면 카운트하라.
}

const str = 'KoreaTimeGood'
solution(str)
```


### 풀이 2
```
function solution(str) {
    let answer = 0

    for(let x of str){
        // x의 값이 대문자라면, answer를 카운터해라.
        if(x === x.toUpperCase()) answer++
    }
    return answer
}

const str = 'KoreaTimeGood'
solution(str)

```