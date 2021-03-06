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
---
### :star2:조건문

>if
```
const a = 1;
if (a + 1 === 2) {
 console.log('a + 1 이 2 입니다.');
 console.log('blabla'); // 여러줄 가능
}

const a = 1; // 다른 블록에 있기 때문에 똑같은 이름으로 선언 가능
if (a + 1 === 2) {
 const a = 2; // 다른 블록에 있기 때문에 똑같은 이름으로 선언 가능
 console.log('if문 안의 a 값은 ' + a);
}
console.log('if문 밖의 a 값은 ' + a);

// 값 : if 문 안의 a 값은 2
   값 : if 문 밖의 a  값은 1

//(var을 쓰게 되면 값이 같아짐 - 권장하지 않음)
```

>if else
```
const a = 10;
if (a > 15) {
 console.log('a가 15보다 큽니다.');
} else {
 console.log('a가 15보다 크지 않습니다.');
}
//값 : a가 15보다 크지 않습니다.
```

>if else if
```
const a = 7;

if (a === 5) {
 console.log('5 입니다!');
} else if (a === 10) {        // else if 는 여러개 사용 가능
 console.log('10 입니다!');
} else {
 console.log('5도 아니고 10도 아닙니다.');
}
// 값 : 5도 아니고 10도 아닙니다.
```
---
### :star2:조건문
>switch case
```
const device = 'iphone';

switch (device) {
 case 'iphone';
  console.log('아이폰!');
  break; // 비교가 끝났다는 표시, 브레이크를 안하면 다음 코드까지 실행
 case 'ipad':
  console.log('아이패드!');
  break;
 case 'galaxy note';
  console.log('갤럭시 노트!');
  break;
 default; // 아무것도 해당되지 않는경우
  console.log('모르겠네요..');
}
// 값 : 아이폰!
```
```
const device = 'ipad';

switch (device) {
 case 'iphone';
  console.log('아이폰!');
  break;
 case 'ipad':
  console.log('아이패드!');
  break;
 case 'galaxy note';
  console.log('갤럭시 노트!');
  break;
 default;
  console.log('모르겠네요..');
}
// 값 : 아이패드!
```
```
const device = 'galaxy note';

switch (device) {
 case 'iphone';
  console.log('아이폰!');
  break;
 case 'ipad':
  console.log('아이패드!');
  break;
 case 'galaxy note';
  console.log('갤럭시 노트!');
  break;
 default;
  console.log('모르겠네요..');
}
// 값 : 갤럭시 노트!
```
```
const device = 'macbook';

switch (device) {
 case 'iphone';
  console.log('아이폰!');
  break;
 case 'ipad':
  console.log('아이패드!');
  break;
 case 'galaxy note';
  console.log('갤럭시 노트!');
  break;
 default;
  console.log('모르겠네요..');
}
// 값 : 모르겠네요..
```
---
### :star2:함수
<img src="https://user-images.githubusercontent.com/86407453/131250079-f94e3c85-a01d-496a-83dc-0cee3a2bde2b.PNG">

```
const a = 1;
const b = 2;
const sum = a + b;
```

함수로 변경:point_down:

```
function add(a, b) {       // (파라미터 : 함수에서 받아오는 값)
 return a + b;
} // add라는 함수를 만든 것

const sum = add(1, 2);
console.log(sum);
// 값 : 3
```
<img src="https://user-images.githubusercontent.com/86407453/131250118-a0335a9c-09f3-410d-bfe6-9ff0e24f3878.PNG">

```
function hello(name) {
 console.log('Hello, ' + name + '!');
}

hello('seohee');
// 값 : Hello, seohee!
```
---
2021.08.30
### :star2:함수 Template Literal

```
function hello(name) {
 console.log(`Hello ${name}!`);
}

hello('seohee');
// 값 : Hello seohee!
```

```
function hello(name) {
 return `Hello ${name}!`;    //return이 사용되는 순간 함수는 종료됨
}

const result = hello('seohee');
console.log(result);
// 값 : Hello seohee!
```
---
>함수 연습
```
function getGrade(score) {
 if (score === 100) {
  return 'A+';
 } else if (score >= 90) {
   return 'A'; 
 } else if (score === 89) {
   return 'B+';
 } else if (score >= 80) {
   return 'B';
 } else if (score === 79) {
   return 'C+';
 } else if (score >= 70) {
   return 'C';
 } else if (score === 69) {
   return 'D+';
 } else if (score >= 60) {
   return 'D';
 } else {
   return 'F';
 }
}
const grade = getGrade(100);
console.log(grade);
// 값 : A+

const grade = getGrade(95);
console.log(grade);
// 값 : A

const grade = getGrade(89);
console.log(grade);
// 값 : B+

const grade = getGrade(83);
console.log(grade);
// 값 : B

const grade = getGrade(70);
console.log(grade);
// 값 : C

const grade = getGrade(69);
console.log(grade);
// 값 : D+

const grade = getGrade(30);
console.log(grade);
// 값 : F
```
---
### :star2:화살표 함수
```
const add = (a, b) => {
 return a + b;
}

const sum = add(1, 2);
console.log(sum);

// 값 : 3
```

```
const add = (a, b) => a + b;

const hello = (name) => {
 console.log(`Hello, ${name}!`);
}

hello('seohee');

// 값 : Hello, seohee!
```

```
const add = (a, b) => a + b;

const sum = add(1, 2);
console.log(sum);

// 값 : 3
```
---
2021.08.31
### :star2:객체

```
const dogName = '멍멍이';
const dogAge = 2;

console.log(dogName);
console.log(dogAge);
```

:point_down:

```
const dog = {
 name: '멍멍이',
 age: 2,
 cute: true,
 sample: {
  a: 1,
  a: 2,
 }
}
```

:point_down:

```
const dog = {
 name = '멍멍이',
 age = 2,
 'key with space': 'asdf',     // 공백 쓸 수 없음
}

console.log(dog);
console.log(dog.name);
console.log(dog.age);

// 값 : Object {name: "멍멍이", age: 2, key with space: asdf}
         name: "멍멍이"
         age: 2
         key with space: "asdf"
     
         멍멍이
         2
```

```
const ironMan = {
 name: '토니 스타크',
 actor: '로버트 다우니 주니어',
 alias: '아이언맨'
};

const captainAmerica = {
 name: '스티븐 로저스',
 actor: '크리스 에반스',
 alias: '캡틴 아메리카'
};

console.log(ironMan);
console.log(captainAmerica);

// 값 : Object{ name: "토니스타크", actor: ~}
        Object{ name: "스티븐 로저스", actor: ~}
```

```
const ironMan = {
 name: '토니 스타크',
 actor: '로버트 다우니 주니어',
 alias: '아이언맨'
};

const captainAmerica = {
 name: '스티븐 로저스',
 actor: '크리스 에반스',
 alias: '캡틴 아메리카'
};

function print(hero) {
 const text = `${hero.alias}(${hero.name}) 역할을 맡은 배우는 ${hero.actor} 입니다.`;
 console.log(text);
}

print(ironMan);
print(captainAmerica);

// 값 : 아이언맨(토니 스타크) 역할을 맡은 배우는 로버트 다우니 주니어 입니다.
        캡틴 아메리카(스티븐 로저스) 역할을 맡은 배우는 크리스 에반스 입니다.
```
---
### :star2:객체 - 비구조화 할당 (객체 구조 분해)

```
const ironMan = {
 name: '토니 스타크',
 actor: '로버트 다우니 주니어',
 alias: '아이언맨'
};

const captainAmerica = {
 name: '스티븐 로저스',
 actor: '크리스 에반스',
 alias: '캡틴 아메리카'
};

function print(hero) {
 const { alias, name, actor } = hero;
 const text = `${alias}(${name}) 역할을 맡은 배우는 ${actor} 입니다.`;
 console.log(text);
}

print(ironMan);
print(captainAmerica);

// 값 : 아이언맨(토니 스타크) 역할을 맡은 배우는 로버트 다우니 주니어 입니다.
        캡틴 아메리카(스티븐 로저스) 역할을 맡은 배우는 크리스 에반스 입니다.
```

```
const ironMan = {
 name: '토니 스타크',
 actor: '로버트 다우니 주니어',
 alias: '아이언맨'
};

const captainAmerica = {
 name: '스티븐 로저스',
 actor: '크리스 에반스',
 alias: '캡틴 아메리카'
};

function print({ alias, name, actor }) {
 const text = `${alias}(${name}) 역할을 맡은 배우는 ${actor} 입니다.`;
 console.log(text);
}

print(ironMan);
print(captainAmerica);

// 값 : 아이언맨(토니 스타크) 역할을 맡은 배우는 로버트 다우니 주니어 입니다.
        캡틴 아메리카(스티븐 로저스) 역할을 맡은 배우는 크리스 에반스 입니다.
```

```
const ironMan = {
 name: '토니 스타크',
 actor: '로버트 다우니 주니어',
 alias: '아이언맨'
};

const { name } = ironMan;
console.log(name);

const captainAmerica = {
 name: '스티븐 로저스',
 actor: '크리스 에반스',
 alias: '캡틴 아메리카'
};

function print({ alias, name, actor }) {
 const text = `${alias}(${name}) 역할을 맡은 배우는 ${actor} 입니다.`;
 console.log(text);
}

print(ironMan);
print(captainAmerica);

// 값 : 토니스타크
        아이언맨(토니 스타크) 역할을 맡은 배우는 로버트 다우니 주니어 입니다.
        캡틴 아메리카(스티븐 로저스) 역할을 맡은 배우는 크리스 에반스 입니다.
```
---
### :star2: - 객체 안에 함수 넣기

```
const dog = {
 name: '멍멍이',
 sound: '멍멍!',
 say: function say() {        //say, function say 생략 가능. 화살표 함수는 작동X
  console.log(this.sound);
 }
};

dog.say();

// 값 : 멍멍!
```

```
const dog = {
 name: '멍멍이',
 sound: '멍멍!',
 say: function say() {        //say, function say 생략 가능. 화살표 함수는 작동X
  console.log(this.sound);
 }
};

const cat = {
 name: '야옹이',
 sound: '야옹~'
};

cat.say = dog.say;
dog.say();
cat.say();

const catSay = cat.say;   //함수를 꺼내면 this와의 관계가 사라짐
cat.Say();

// 값 : 멍멍!
        야옹~
        Error in ...
```
---
### :star2:객체 - Getter 와 Setter 함수

>Getter (특정 값을 조회 할 때 마다)

```
const numbers = {
 a: 1,
 b: 2
};

numbers.a = 5;
console.log(numbers);

// 값 : Object {a: 5, b: 2}
```

:point_down:

```
const numbers = {
 a: 1,
 b: 2
  get sum() {
   console.log('sum 함수가 실행됩니다!');
   return this.a + this.b;
 }
};

console.log(number.sum);
numbers.b = 5;
console.log(numbers.sum);

// 값 : sum 함수가 실행됩니다!
        3
        sum 함수가 실행됩니다!
        6
```

>Setter (특정 값을 설정 할 때 마다)

```
const dog = {
  _name: '멍멍이',
  set name(value) {
    console.log('이름이 바귑니다..' + value);
    this._name = value;
  }
};

console.log(dog._name);
dog.name = '뭉뭉이';
console.log(dog._name);

// 값 : 멍멍이
         이름이 바뀝니다..뭉뭉이
         뭉뭉이 
```

```
const numbers = {
  _a: 1,
  _b : 2,
  sum: 3,
  calculate() {
    console.log('calculate');
    this.sum = this._a + this._b;
  },
  get a() {
    return this._a;
  },
  get b() {
    return this._b;
  },
  set a(value) {
    this._a = value;
    this.calculate();
  },
  set b(value) {
    this._b = value;
    this.calculate();
  }
};

console.log(numbers.sum);
numbers.a = 5;
numbers.b = 7;
numbers.a = 9;
console.log(numbers.sum);
console.log(numbers.sum);
console.log(numbers.sum);

// 값 : 3
        calculate
        calculate
        calculate
        16
        16
        16
```
