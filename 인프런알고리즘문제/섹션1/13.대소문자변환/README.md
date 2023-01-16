## 대소문자변환
- 대문자와 소문자가 같이 존재하는 문자열을 입력받아 대문자는 소문자로 소문자는 대문자로 변환하여 출력하는 프로그램을 작성하세요.

## 입력예제
- 1 StuDY

##  출력예제 
- 1 sTUdy


## 내가 푼 방법
```
function solution(str) {
    let answer = []
    // 문자를 반복문을 돌려 하나씩 확인
    // 소문자라면 대문자로
    // 대문자라면 소문자로

    for(let x of str){
        if(x === x.toUpperCase()){
            answer.push(x.toLowerCase())
        } else {
            answer.push(x.toUpperCase())
        }
    }
    return answer
    
    
}
solution("StuDY")
```
