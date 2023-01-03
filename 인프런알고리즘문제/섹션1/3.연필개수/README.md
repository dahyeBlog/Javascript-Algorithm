## 연필개수
- 연필 1다스는 12자루이고, 학생 1인당 연필을 1자루씩 나누어 준다고 할 떄, N명이 학생수를 입력하면 필요한 연필의 다스 수를 계산하는 프로그램을 작성하라. 

### 풀이방법
```
//풀이
  function pensil(n) {
    let das = Math.ceil(n / 12)
      return das
  }
```

### Math.ceil()
- Javascript에서 숫자를 올림 처리할 때 사용
- 음수를 포함해서 입력받은 숫자보다 크거나 같은 정수 중, 가장 작은 정수를 리턴한다. 

```
// 1.올림
const ceil_1 = Math.ceil(1); // 1
const ceil_2 = Math.ceil(1.222); // 2
const ceil_3 = Math.ceil(1.5); // 2
const ceil_4 = Math.ceil(1.777); // 2

// 2. null 또는 0인 경우
const ceil_5 = Math.ceil(null); // 0
const ceil_6 = Math.ceil(0); // 0

// 3. 음수인 경우
const ceil_7 = Math.ceil(-1); // -1
const ceil_8 = Math.ceil(-1.111); // -1
const ceil_9 = Math.ceil(-1.5); // -1
const ceil_10 = Math.ceil(-1.777); // -1
```