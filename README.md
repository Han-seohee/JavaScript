# JavaScript 자바스크립트 이론
2021.08.25
### :star2:변수
```
let value = 1; 
console.log(value);
//특정 이름에 특정 값을 넣는것 (선언)

value = 2;
console.log(value);
// 값을 바꿀 수 있음

let value = 2; //error - 한 번 선언 했으면 똑같은 이름으로 선언 불가
```

### :star2:상수
```
const a = 1; //한번 값을 설정하고 나면 바꾸지 못함
a = 2; //error
const a = 2; //error
```
### :star2:데이터 타입
>숫자
```
let value = 100;
```
>문자
```
let text = 'hello';
let text = "헬로우";
```
>Boolean
```
let good = true;
let loading = false;
```
>null (없다)
```
let good = null;
//ex) let friend = null;
```
>undefined (아직 정해지지 않았다)
```
let something = undefined; 
//ex) let criminal;
      console.log(criminal);
```
---
2021.08.26
### :star2:대입연산자
```
let value = 1;

let a = 1;
a += 1; // a에 1을 더하겠다
a -= 3;
a *= 3;
console.log(a);
```

### :star2:산술연산자
```
let a = 1 + 2 - (3 * 4) / 4 ;
console.log(a);
```
```
let a = 1;
console.loa(a++);  값 : 1 // 보여준 다음에 계산을 하느냐
console.log(a); 값: 2
console.log(++a); 값: 3 // 미리 계산을 하고 보여주느냐

let a = 1;
console.loa(a--);  값 : 1
console.log(a); 값: 0
```
