# JavaScript Core Syntax

## 1. 변수

변수는 값을 저장할 때 사용한다.

```js
let age = 16;
const name = "Yerin";

age = 17;
```

`let`은 값을 다시 할당할 수 있고, `const`는 재할당할 수 없다.

## 2. 자료형

JavaScript에서 자주 사용하는 자료형은 다음과 같다.

- `string` : 문자열
- `number` : 숫자
- `boolean` : `true` / `false`
- `object` : 여러 값을 묶어서 저장

```js
const name = "Yerin";
const age = 16;
const isStudent = true;
```

객체는 key와 value를 묶어서 저장할 수 있다.

```js
const user = {
  name: "Yerin",
  age: 16,
};
```

## null과 undefined

둘 다 값이 없다는 의미로 사용되지만 상황이 다르다.

- `undefined` : 값이 아직 할당되지 않은 상태
- `null` : 개발자가 의도적으로 값이 없다고 지정한 상태

```js
let a;
let b = null;

console.log(a); // undefined
console.log(b); // null
```

## 3. 조건문

조건에 따라 다른 코드를 실행할 때 사용한다.

```js
if (age >= 17) {
  console.log("17살 이상");
} else {
  console.log("17살 미만");
}
```

조건이 여러 개라면 `else if`를 사용할 수 있다.

`===`는 값과 자료형을 모두 비교하기 때문에 보통 `==`보다 `===`를 사용한다.

## 4. 반복문

같은 코드를 여러 번 실행할 때 사용한다.

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

배열의 값을 하나씩 확인할 때는 `for...of`를 사용할 수 있다.

```js
const fruits = ["apple", "banana", "grape"];

for (const fruit of fruits) {
  console.log(fruit);
}
```

## 5. Scope

Scope는 변수를 사용할 수 있는 범위를 의미한다.

```js
let name = "Yerin";

if (true) {
  let age = 16;
  console.log(age);
}

console.log(name);
```

`let`과 `const`로 선언한 변수는 선언된 블록 `{}` 안에서 사용할 수 있다.

```js
if (true) {
  const message = "Hello";
}

console.log(message); // 오류
```

함수 안에서 선언한 변수도 함수 밖에서는 사용할 수 없다.

```js
function test() {
  const value = 10;
}

console.log(value); // 오류
```

즉, 변수는 **어디에서 선언했는지에 따라 사용할 수 있는 범위가 달라진다.**


## 6. 정리

- `let`, `const`로 변수를 선언한다.
- 자료형에 따라 저장되는 값의 형태가 다르다.
- `if`문으로 조건에 따라 코드를 실행할 수 있다.
- 반복문으로 같은 작업을 반복할 수 있다.
