## 문자열 압축
- 알파벳 대문자로 이루어진 문자열을 입력받아 같은 문자가 연속으로 반복되는 경우 반복되는 문자 바로 오른쪽에 반복 횟수를 표기하는 방법으로 문자열을 압축하는 프로그램을 작성하시 오. 단 반복횟수가 1인 경우 생략합니다.

## 입력설명
- 첫 줄에 문자열이 주어진다. 문자열의 길이는 100을 넘지 않는다.

## 출력설명
- 첫 줄에 압축된 문자열을 출력한다.

##  입력예제 1
- KKHSSSSSSSE

##  출력예제 1 
- K2HS7E


## 강의 풀이법
```
// 문자열 내 문자열 두개 비교해서 같으면 카운팅하기
// 다른 경우 answer에 문자 누적하고
// 개수도 문자열로 바꿔서 answer에 누적함.


 function solution(s){
     let answer=""; 
     let cnt=1; //제일 앞에 문자하나는 기본으로 있어야하므로 1로저장

  for(let i=0;i<s.length;i++){
   if(s[i] === s[i+1] ) {
    cnt++
   }else {
    answer+=s[i] // answer에 문자누적해줘야함
    if(cnt > 1){ // count가 1보다 크면 문자로 바꿔서 answer에 누적
     answer+=String(cnt) // count는 다시 1로 초기화시켜준다. 
     cnt = 1
    }
   }
  }

     return answer;
 }
            
let str="KKHSSSSSSSE";
solution(str)
```