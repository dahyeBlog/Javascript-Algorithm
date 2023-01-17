## 큰 수 출력하기
- N(1<=N<=100)개의 정수를 입력받아, 자신의 바로 앞 수보다 큰 수만 출력하는 프로그램을 작성하세요. (첫 번째 수는 무조건 출력한다.)

##  입력예제 1
- 7 3 9 5 6 12

##  출력예제 1 
- 7 9 6 12

## 내가 푼 방법
```
function solution(str) {
 let answer = []
    
   // 루프를 돌려, 서로 비교한 후 가장 큰 수 배열에 할당.
    answer.push(str[0])
    // 첫 번째 수는 무조건 출력하기 위해 answer에 할당
    for(let i=0;i<str.length;i++){
        if(str[i-1]<str[i]){
            answer.push(str[i])
        }
    }
    return answer
}

const str=[7,3,9,5,6,12]
solution(str)
```

