# JavaScript Asynchronous

## 1. Promise

시간이 걸리는 작업의 결과를 처리하기 위해 `Promise`를 사용한다.

Promise는 작업 상태에 따라 `pending`, `fulfilled`, `rejected` 상태를 가진다.

```js
const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("성공");
  } else {
    reject("실패");
  }
});
```

## 2. then / catch

`then()`은 작업이 성공했을 때, `catch()`는 실패했을 때 실행된다.

```js
promise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

## 3. async / await

Promise를 조금 더 읽기 쉽게 작성할 수 있다.

```js
async function getData() {
  const result = await promise;
  console.log(result);
}
```

`async`가 붙은 함수는 Promise를 반환하고, `await`는 Promise가 처리될 때까지 기다린다.

## 4. fetch

`fetch()`를 사용하면 서버에 HTTP 요청을 보낼 수 있다.

```js
const response = await fetch("https://example.com");
const data = await response.json();

console.log(data);
```

`fetch()`의 결과는 `Response` 객체로 받고, `response.json()`을 통해 응답 데이터를 사용할 수 있는 형태로 변환한다.

## 5. HTTP 요청

자주 사용하는 HTTP 메서드는 다음과 같다.

* `GET` : 데이터 조회
* `POST` : 데이터 생성
* `PUT` : 데이터 수정
* `DELETE` : 데이터 삭제

POST 요청에서는 데이터를 JSON 형태로 보내기도 한다.

```js
fetch("https://example.com", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    name: "Yerin"
  })
});
```

## 6. 응답 확인

`response.ok`를 사용하면 요청이 성공했는지 확인할 수 있다.

```js
if (!response.ok) {
  throw new Error("요청 실패");
}
```

HTTP 상태 코드는 서버의 요청 결과를 나타낸다.

* `2xx` : 성공
* `4xx` : 클라이언트 오류
* `5xx` : 서버 오류

## 정리

Promise를 이용해 비동기 작업을 처리할 수 있고, `async/await`를 사용하면 비동기 코드를 좀 더 쉽게 작성할 수 있다.

`fetch()`를 이용하면 서버와 데이터를 주고받을 수 있으며, HTTP 메서드와 응답 상태를 함께 이해하는 것이 중요하다.
