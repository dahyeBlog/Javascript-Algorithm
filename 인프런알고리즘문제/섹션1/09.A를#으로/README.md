### A를 #으로
대문자로 이루어진 영어단어가 입력되면 단어에 포함된 ‘A'를 모두 ’#‘으로 바꾸어 출력하는 프로그램을 작성하세요.

### replace()
- replace() 메서드는 어떤 패턴에 일치하는 일부 또는 모든 부분이 교체된 새로운 문자열을 반환한다. 
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/String/replace

### 풀이
```
function solution(str) {
  let answer = ""
  // 루프를 돌려 문자열 확인
  for(let i of str) {
    // 대문자 A인지 확인
    // A이면, #로 바꾸기.
    if(i === "A"){
      i = "#"
    }
      answer+=i
 }
return answer
}
solution('BANANA')
```
### 풀이 2
```
function solution(str) {
  let answer = ""

  for(let x of str) {
    if(x ==='A') answer+="#"
    else answer+=x
  }
  return answer
}


solution('BANANA')
```
### 풀이 3
```
function solution(str) {
  let answer = str

  answer = answer.replace(/A/g, '#')
  
  
  return answer
}


solution('BANANA')
```