## 중복문자제거
- 소문자로 된 한개의 문자열이 입력되면 중복된 문자를 제거하고 출력하는 프로그램을 작성하세요. 제거된 문자열의 각 문자는 원래 문자열의 순서를 유지합니다. 

##  입력예제 1
- ksekkset

##  출력예제 1 
- kset

## 내가 푼 방법
```
function solution(str) {

    let answer = ""

   for(let i=0; i<str.length;i++){
       if(str.indexOf(str[i])===i){
           // str[i]의 string의 인덱스를 찾아 인덱스 i와 같으면
           // answer에 i인덱스 문자열 할당
           answer+=str[i]
       }
   }
    

    return answer
    }

solution('ksekkset')
```


### indexOf 메서드
- string.indexOf(searchvalue, position)
- indexOf함수는, 문자열에서 특정 문자열을 찾고, 검색된 문자열이 '첫번째'로 나타나는 위치 index를 리턴한다. 

