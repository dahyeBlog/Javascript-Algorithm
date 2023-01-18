## 가위 바위 보
- A,B 두 사람이 가위 바위 보 게임을 한다. 총 N번의 게임을 하여 A가 이기면 A를 출력하고, B가 이기면 B를 출력한다. 비길 경우에는 D를 출력한다. 
- 가위, 바위, 보 의 정보는 1:가위, 2:바위, 3:보 
- 예를 들어 N=5이면
[./img.png]

##  입력예제 1
- 23313 11223

##  출력예제 1 
- A B A B D

## 내가 푼 방법
```

function solution(a,b) {
    let answer = ""

    for(let i = 0; i< a.length; i++){

       if(a[i] === b[i]) answer += "D"

        else if(a[i] === 1 && b[i] === 2) answer+="B"
        else if (a[i] === 2 && b[i] === 3) answer+="B"
        else if (a[i]===3 && b[i] === 1) answer+="B"
        else answer+="A"
    }
    return answer
}

 let a=[2, 3, 3, 1, 3];
 let b=[1, 1, 2, 2, 3];

solution(a,b)
```