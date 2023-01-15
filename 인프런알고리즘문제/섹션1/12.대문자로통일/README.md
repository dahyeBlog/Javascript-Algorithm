## 대문자로 통일
- 대문자와 소문자가 같이 존재하는 문자열을 입력받아, 대문자로 모두 통일하여 문자열을 출력하는 프로그램을 작성하세요.

### 내가 푼 풀이 
```
function solution(str) {
    let answer = ""

    // 문자열을 받아와 루프를 돌려, 소문자를 대문자로 바꾼다.
    for(let x of str){
    // x의 값이 대문자이면, answer에 할당하기
     if(x === x.toUpperCase()){
         answer += x
    // 아니면 x의 값을 대문자로 바꿔 answer에 할당하라.
     } else {
        answer += x.toUpperCase()
     }
    }
 
    return answer
}

const str = 'ItisTimeToStudy'
solution(str)
```
