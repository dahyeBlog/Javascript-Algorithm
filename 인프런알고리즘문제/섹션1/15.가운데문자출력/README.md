## 가운데 문자 출력
- 소문자로 된 단어(문자열)가 입력되면 그 단어의 가운데 문자를 출력하는 프로그램을 작성하세요. 단 단어의 길이가 짝수일 경우 가운데 2개의 문자를 출력한다. 

##  입력예제 1
- study
- good

##  출력예제 1 
- u
- oo

## 내가 푼 방법
```
function solution(str) {

    let answer = ""
    // 중간 인덱스 값을 찾는다.
    // 각 문자를 spilt메서드로 나눈다
    // 만약 문자열의 가운데 값이 홀수이면, 중간 인덱스 값을 구한다. 
    // 중간 값이 아니라면 중간 인덱스값과 이전 인덱스 값을 구한다. 
    let midIndex = parseInt(str.length / 2)

    if(str.length%2 === 0 ){
      answer += str.split("")[midIndex-1]
      answer += str.split("")[midIndex]
    } else {
       answer += str.split("")[midIndex]

    }


    return answer
    }

solution('study')
```

## 풀이법
```
function solution(str) {

    let answer = ""
    // 중간 인덱스값 구하기 
    let mid = Math.floor(str.length/2)
    if(str.length%2 === 1){
        answer = str.substring(mid, mid+1)
    }else {
        answer = str.substring(mid-1, mid+1)
    }
    


    return answer
    }

solution('good')
```

### substring 메서드
- string 객체의 시작 인덱스로 부터 종료 인덱스 전까지 문자열의 부분 문자열을 반환한다. 
