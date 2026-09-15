# JavaScript Functions

## 1. 함수

함수는 특정 작업을 하나로 묶어두고 필요할 때 호출해서 사용할 수 있다.

```js
function greet() {
  console.log("Hello");
}

greet();
```

## 2. 매개변수

함수를 호출할 때 값을 전달할 수 있다.

```js
function greet(name) {
  console.log(`Hello, ${name}`);
}

greet("Yerin");
```

`name`처럼 함수에서 전달받는 값을 **매개변수**라고 한다.

## 3. return

`return`을 사용하면 함수의 결과를 밖으로 반환할 수 있다.

```js
function add(a, b) {
  return a + b;
}

const result = add(2, 3);

console.log(result);
```

`console.log()`는 값을 출력하는 것이고, `return`은 함수의 결과를 반환하는 것이라는 차이가 있다.

## 4. 화살표 함수

함수를 조금 더 간단하게 작성할 수 있다.

```js
const add = (a, b) => {
  return a + b;
};
```

실행할 코드가 한 줄이면 중괄호와 `return`을 생략할 수도 있다.

```js
const add = (a, b) => a + b;
```

## 5. 정리

* 함수는 특정 작업을 묶어 재사용할 수 있다.
* 매개변수를 통해 함수에 값을 전달할 수 있다.
* `return`으로 함수의 결과를 반환할 수 있다.
* 화살표 함수는 함수를 간단하게 표현할 때 사용한다.
