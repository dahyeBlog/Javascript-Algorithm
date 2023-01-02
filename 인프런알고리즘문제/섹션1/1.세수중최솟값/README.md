## 세수중 최솟값
- 100이하의 자연수 a,b,c 중 가장 작은 값(최솟값)을 출력하라.

### 내가 푼 풀이 방법
```
           function min(a,b,c) {
              let minText; // 최솟값을 담을 수있는 변수 정의하고

               minText = Math.min(a,b,c) // Math.min()메서드를 사용함.

              return minText

         }
          console.log(min(56,25,1));

```

### 다른 풀이 방법
```
        //풀이2
        function min(a,b,c) {
            let minText; 
            if(a>b && c>b) {  // b가 가장 작은 값이면,
                return minText = b //b의 값을 반환
            } else if (c > a && b > a) { //a의 값이 가장 작은 값이라면, 
                return minText = a //a반환
            } else {
                return minText = c //c반환
            }
        }
            
        console.log(min(61,52,11));
        

        //풀이3

        function min(a,b,c) {
            let answer;
            if(a<b) answer = a
            else answer = b
            if(c < answer) answer = c
            return answer 
        }

        console.log(min(2,5,1));
```