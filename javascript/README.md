# Study-JS
---
## 20210519

### <b>Javascript
---
#### Expression (표현식)
값을 만듦 > 함수의 인자로 사용 가능

#### Statement
하나 or 여러 표현식이 문장을 이룸
모든 표현식은 문장이 될 수 있음
문장끝에 세미클론 ;
한 줄에 여러문장을 적을 경우, 세미콜론으로 문장을 구분해야 함(;)
마지막 문자의 결과가 반환
조건문(if), 반복문(for)도 문장
마지막 <b>(}) (; 세미콜론 생략)

#### Reserved Words(예약어)
변수명, 함수명 등으로 지정 불가

#### Identifier(식별자)
코드 내의 변수, 함수 등을 식별
대소문자 구문
유니코드문자, $, _, 숫자 사용가능하나, 숫자로 시작할순 없음
```js
var name = '태영';
```
역할에 맞는 적절한 이름을 지어야함

#### 변수의 유효 범위
##### 블록 스코프 {}
const, let 등 블록 스코프{}
중괄호 {} = 블록
##### 함수 스코프(var)
function(){}

#### Hoisting
선언 vs 호출 순서오류?

아래의 함수, 변수 등의 선언(만) 호출해옴

#### Data Types
Boolean (T/F)
Null (값이 없음을 나타내는 object)
Undefined ()
Number ()
String ()
템플릿 스트링 `${a} ddd`
Symbol ()

Object (객체)

#### 조건문(if)
```js
if (true){
    console.log('항상 실행')
}

if (false){
    console.log('항상 실행 X')
}

```
표현식이 거짓으로 평가 Falsy
- false, 0, 빈 문자열'', null, undefined, NaN
```js
if (false) console.log(false);
if (0) console.log(false);
if ('') console.log('');
if (null) console.log(null);
if (undefined) console.log(undefined);
if (NaN) console.log(NaN);
```

표현식이 참으로 평가 Treuthy
- true, 0이 아닌 숫자, 문자열'', {}, []
```js
if (true) console.log(true);
if (28) console.log(28);
if (-28) console.log(-28);
if ('taeyoung') console.log('taeyoung');
if ({}) console.log({});
if ([]) console.log([]);
```

#### 조건문(else)
```js
const n = 28;
if (n>0) {
    console.log('n이 0보다 큰 경우')
}   else {
    console.log('n이 0보다 크지 않은경우')
}
```

#### 논리연산자 평가 (&&, ||,!)

&&(and) - tt=t, tf=f, ft=f, ff=f

||(or) - tt=t, tf=t, ft=t, ff=f

!(not) - !t=f, !f=t

#### switch 조건문

3항 연산자 활용

```js
let n = 5;
concole.log(n % 5 === 0 ? '5의 배수' : '5의 배수아님 ')
```

```js
let n = 5;
switch (n) {
    default:
        console.log(n);
}
```


#### 반복문(for)
```js
console.log('hello');
console.log('hello');
console.log('hello');
console.log('hello');
console.log('hello');
```
```js
for (let i = 0; i < 5; i++){
    console.log('hello');
}
```

for (초기화; 반복 조건; 반복이 된후 실행되는 코드){
    코드블럭
}

for (a; b; c;){
    d
}
    e

a > d > c > b > d > b > e 


for(;;){
    d
}

d가 무한히 반복


#### while 반복문
while(조건){
    조건이 거짓이 될 때까지 반복
}

do {
    조건이 거짓이 될 때까지 반복
} while(조건);


for of - iterable한 객체 (ex. array)
```js
for (const i of [1, 2, 3]){
    console.log(i);
}
```



for in - 모든 프로퍼티 (객체 내부의 프로퍼티를)


#### function
<b>선언적함수
function 함수명() {
    함수의 바디
}

(매개변수) - 함수 호출 값 지정

<b>익명함수
const 함수명 = function(){
    함수의 바디
}

<b>arrow 함수
const hello1 - () => {
    console.log('hello1');
}

<b>new 함수
funtion person(name, age){
    this.name = name;
    this.age = age;
}

const p = new person('mark', 27);
console.log(p,p.name, p.age);

const a = new person('anna', 24);
console.log()


```js
board = [[0,0,0,0,0],[0,0,1,0,3],[0,2,5,0,1],[4,2,4,4,2],[3,5,1,3,1]]
moves = [1,5,3,5,1,2,1,4]

function solution(board, moves) {
    var answer = 0;
    return answer;
}
```