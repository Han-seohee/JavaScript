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
console.loa(a++); // 값: 1 (보여준 다음에 계산을 하느냐)
console.log(a); // 값: 2
console.log(++a); // 값: 3 (미리 계산을 하고 보여주느냐)

let a = 1;
console.loa(a--); //값 : 1
console.log(a); //값: 0
```
---
2021.08.27
### :star2:논리연산자
Boolean을 처리하기 위한 연산자

1. NOT 연산자 !
```
const a = !true; // 값: false
const a = !false; // 값: true
console.log(a);
```

2. AND 연산자 &&
```
const a = true && true; // 값: true 양쪽이 모두 true일 때만 true
const a = false && true; // 값: false
const a = true && false; // 값: false
const a = false && false; // 값: false
console.log(a);
```

3. OR 연산자 ||
```
const a = true || true; // 값: true
const a = false || true; // 값: true
const a = true || false; // 값: true
const a = false || false; // 값: false 양쪽이 모두 false일 때만 false
console.log(a); 
```

> NOT > AND > OR 순서
```
const value = !(true && false || true && false || !false);
// !(true && false || true && false || true)
// !(false || false || true)
// !(true)
// false
console.log(value); //값: false
```
---
2021.08.29
### :star2:비교연산자
두 값을 비교 할 때 쓰는 연산자

>equals
```
const a = 1;
const b = 1;
const equals = a === b; 
console.log(equals);
// 값 : true

const a = 1;
const b = 2;
const equals = a === b;
console.log(equals);
// 값 : false

// Use 'equals' three times to compare the two values.
// (equals 사인을 두번 입력하면 타입을 검사하지 않기 때문에 세개를 쓸것을 권장함)
```

>notEquals
```
const a = 1;
const b = '1';
const notEquals = a !== b; 
console.log(notEquals);
// 값 : true
```

>크고 작음을 비교
```
const a = 10;
const b = 15;
const c = 15;

console.log(a < b); //값 : true
console.log(a > b); //값 : true
console.log(b >= a); //값 : true
console.log(a <= c); //값 : true
console.log(b < c); //값 : false
```

### :star2:문자열 붙이기
```
const a = '안녕';
const b = '하세요';
console.log(a + b);
// 값 : 안녕하세요
```
