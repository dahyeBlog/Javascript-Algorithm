## 1부터 N까지 합 출력하기
- 자연수 n이 입력되면, 1부터 n까지의 합을 출력하는 프로그램을 작성하라. 

### 풀이방법

//풀이방법 1
//시간복잡도 O(n)
```
  function sum(n) {
      let sumNum = 0
      for (let i = 0; i <= n; i++) {
        sumNum += i
      }
        return sumNum
      }
        sum(6)
```

//풀이방법2
//시간복잡도 O(1)
```

  function sum(n) {
  return n * (n + 1) / 2
}

sum(6)


```