## 중복단어제거
- N개의 문자열이 입력되면 중복된 문자열은 제거하고 출력하는 프로그램을 작성하세요. 출력하는 문자열은 원래의 입력순서를 유지한다. 

##  입력예제 1
```
5
good
time
good 
time 
student
```

##  출력예제 1 
```
good
time
student
```

## 내가 푼 방법
```
function solution(str) {

    let answer = []

    // 문자열을 루프를 돌린다.

    for(let i=0; i<str.length;i++){
       if(str.indexOf(str[i]) === i){
           answer.push(str[i])
       }
    }
    

    return answer
    }

const str= ['good','time','good','time','student']
solution(str)
```


## 풀이법
```
function solution(str) {

    let answer = []

    answer=str.filter((v,i)=>{
        if(str.indexOf(v) === i) return v
    })

    return answer
    }

const str= ['good','time','good','time','student']
solution(str)
```

### filter()함수
- filter() 메서드는 주어진 함수의 테스트를 통과하는 모든 요소를 모아 새로운 배열로 반환한다.
