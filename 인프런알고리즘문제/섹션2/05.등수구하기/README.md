## 등수구하기
- N(1<=N<=100)명의 학생의 국어점수가 입력되면 각 학생의 등수를 입력된 순서대로 출력하는 프로그램을 작성하세요.
- 입력된 순서대로 등수를 출력한다.


##  입력예제 1
- 87 89 92 100 76

##  출력예제 1 
- 43215

## 내가 푼 방법
```
function solution(arr) {
    let n = arr.length
    let answer = Array.from({length:n},()=>1) // 배열을 1로 초기화하기

    // 이중 for문을 돌려 비교
    for(let i = 0; i< n; i++){
        for(let j = 0; j<n; j++){
            if(arr[i]<arr[j]) answer[i]++
            
        }
    } 
    return answer

}

  let arr=[87, 89, 92, 100, 76];
solution(arr);

```

## Array.from()
- Array.from()메서드는 유사 배열 객체나 반복 가능한 객체를 얕게 복사해 새로운 Array 객체를 만든다. 
