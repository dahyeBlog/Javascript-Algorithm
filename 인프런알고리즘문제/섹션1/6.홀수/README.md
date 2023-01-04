## 홀수
- 7개의 자연수가 주어질때, 이들 중 홀수인 자연수들을 모두 골라 그 합을 구하고, 고른 홀수들 중 최소값을 찾는 프로그램을 작성하라.
- 예를 들어, 7개의 자연수 12,77,38,41,53,92,85가 주어지면 이들 중 
홀수는 77,41,53,85이므로 
그 합은 77 + 41 + 53 + 85 = 256 이되고,
41 < 53 < 77 < 85이므로 홀수들 중 최소값은 41이 된다.

```
  function hol(arr) {
    let answer = []
        let sum = 0,
            min = 1000 //최솟값을 구하기 위해 가장 높은 숫자 지정후 서로 비교
        for (let i = 0; i < arr.length; i++) {
            if (arr[i] % 2 !== 0) { // arr[i]의 값이 홀수 
                sum = sum + arr[i]  
                if (arr[i] < min) 
                    min = arr[i]
            }
        }
        answer.push(sum)
        answer.push(min)
        return answer
    }
    let arr = [12,77, 38,41,53,92,85]
    hol(arr) 
```