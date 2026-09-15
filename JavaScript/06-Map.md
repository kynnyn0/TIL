# JavaScript Map

## 1. Map이란?

`Map`은 **key와 value를 한 쌍으로 저장하는 자료구조**이다.

```js
const user = new Map();

user.set("name", "Yerin");
user.set("age", 16);
```

## 2. 값 가져오기

`get()`을 사용하면 key에 해당하는 값을 가져올 수 있다.

```js
console.log(user.get("name")); // Yerin
```

## 3. 값이 있는지 확인

`has()`를 사용하면 특정 key가 있는지 확인할 수 있다.

```js
console.log(user.has("name")); // true
console.log(user.has("email")); // false
```

## 4. 값 삭제

`delete()`를 사용하면 특정 key와 value를 삭제할 수 있다.

```js
user.delete("age");
```

## 5. Map의 크기

`size`를 사용하면 저장된 데이터의 개수를 확인할 수 있다.

```js
console.log(user.size);
```

## 정리

* `set()` : 데이터 추가 / 변경
* `get()` : 값 가져오기
* `has()` : key 존재 여부 확인
* `delete()` : 데이터 삭제
* `size` : 데이터 개수 확인
