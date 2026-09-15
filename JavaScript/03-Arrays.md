# JavaScript Arrays

## 1. 배열

배열은 여러 개의 값을 하나의 변수에 저장할 때 사용한다.

```js
const fruits = ["apple", "banana", "grape"];

console.log(fruits[0]); // apple
```

배열의 위치는 `0`부터 시작한다.

## 2. 배열 값 변경

인덱스를 이용해서 값을 변경할 수 있다.

```js
fruits[1] = "orange";
```

`length`를 사용하면 배열의 길이를 확인할 수 있다.

```js
console.log(fruits.length);
```

## 3. 배열에 값 추가 / 삭제

```js
fruits.push("melon");   // 마지막에 추가
fruits.pop();           // 마지막 값 삭제

fruits.unshift("kiwi"); // 처음에 추가
fruits.shift();         // 처음 값 삭제
```

## 4. 배열에서 값 찾기

```js
fruits.includes("apple"); // 포함되어 있는지 확인

fruits.indexOf("apple");  // 위치 확인
```

`indexOf()`는 값을 찾지 못하면 `-1`을 반환한다.

```js
const fruit = fruits.find((fruit) => fruit === "apple");
```

`find()`는 조건에 맞는 첫 번째 값을 반환한다.

## 5. 배열 순회

`for`, `for...of`, `forEach()` 등을 이용해서 배열의 값을 하나씩 확인할 수 있다.

```js
fruits.forEach((fruit) => {
  console.log(fruit);
});
```

## 6. 배열 메서드

배열을 원하는 형태로 처리할 때 다양한 메서드를 사용할 수 있다.

```js
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map((number) => number * 2);

const even = numbers.filter((number) => number % 2 === 0);
```

* `map()` : 각 요소를 변환해서 새로운 배열을 만든다.
* `filter()` : 조건에 맞는 요소만 모아서 새로운 배열을 만든다.
* `some()` : 조건을 만족하는 요소가 하나라도 있는지 확인한다.
* `every()` : 모든 요소가 조건을 만족하는지 확인한다.
* `findIndex()` : 조건에 맞는 첫 번째 요소의 인덱스를 반환한다.

## 7. 기타 메서드

```js
numbers.slice(1, 3);
numbers.splice(1, 2);
numbers.reverse();
numbers.concat([6, 7]);
```

`slice()`는 원본 배열을 변경하지 않고, `splice()`는 원본 배열을 변경한다.

## 정리

배열은 데이터를 여러 개 저장하고 관리할 때 사용한다.
메서드마다 원본 배열을 변경하는지, 새로운 값을 반환하는지를 구분해서 사용하는 것이 중요하다.






### 추가 메서드

```js
const fruits = ["apple", "banana", "grape"];

fruits.join(", "); // "apple, banana, grape"
```

`join()`은 배열의 요소를 하나의 문자열로 합친다.

```js
const numbers = [3, 1, 2];

numbers.sort((a, b) => a - b);
```

`sort()`는 배열을 정렬한다.

```js
const numbers = [10, 20, 30];

for (const index in numbers) {
  console.log(index);
}
```

`for...in`은 배열의 인덱스를 순회할 때 사용할 수 있다.

```js
const numbers = [1, 2, 3, 4];

numbers.findIndex((number) => number === 3);
numbers.some((number) => number > 3);
numbers.every((number) => number > 0);
```

* `findIndex()` : 조건에 맞는 첫 번째 요소의 인덱스를 반환한다.
* `some()` : 조건을 만족하는 요소가 하나라도 있는지 확인한다.
* `every()` : 모든 요소가 조건을 만족하는지 확인한다.
