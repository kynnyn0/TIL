# JavaScript DOM

## 1. DOM이란?

DOM(Document Object Model)은 HTML 문서를 JavaScript에서 객체 형태로 다룰 수 있도록 만든 구조이다.

JavaScript를 이용하면 HTML 요소를 가져오거나 내용을 변경할 수 있다.

## 2. HTML 요소 가져오기

`querySelector()`를 사용하면 CSS 선택자를 이용해서 요소를 가져올 수 있다.

```js
const button = document.querySelector(".button");
const title = document.querySelector("h1");
```

## 3. 내용 변경하기

`textContent`를 이용하면 요소의 텍스트를 변경할 수 있다.

```js
title.textContent = "Hello JavaScript";
```

## 4. 이벤트

사용자의 클릭이나 입력 같은 동작에 반응하도록 만들 수 있다.

`addEventListener()`를 사용해서 이벤트를 등록한다.

```js
button.addEventListener("click", () => {
  console.log("버튼 클릭");
});
```

## 5. DOM을 이용한 간단한 기능

JavaScript로 HTML 요소를 가져온 뒤 값을 변경하면 간단한 인터랙션을 만들 수 있다.

```js
const button = document.querySelector(".counter");
const count = document.querySelector(".count");

let number = 0;

button.addEventListener("click", () => {
  number++;
  count.textContent = number;
});
```

버튼을 클릭할 때마다 `number`를 증가시키고, `textContent`를 이용해 화면에 새로운 값을 보여준다.

## 정리

DOM을 이용하면 JavaScript로 HTML 요소를 선택하고 내용을 변경할 수 있다.

`querySelector()`로 요소를 가져오고, `addEventListener()`로 사용자의 동작을 감지한 뒤 원하는 동작을 실행할 수 있다.
