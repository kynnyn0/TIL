# JSX Basic Syntax

## 1. JSX란?

JSX는 JavaScript 코드 안에서 HTML과 비슷한 문법을 작성할 수 있도록 해주는 문법이다.

React에서 화면에 표시할 UI를 표현할 때 사용한다.

```jsx
function App() {
  return <h1>Hello, React!</h1>;
}
```

JSX는 HTML처럼 보이지만 JavaScript 안에서 작성된다.

## 2. JSX 기본 규칙

### 하나의 부모 요소

JSX에서 여러 요소를 반환할 때는 하나의 부모 요소로 감싸야 한다.

```jsx
function App() {
  return (
    <div>
      <h1>Hello</h1>
      <p>Welcome!</p>
    </div>
  );
}
```

불필요한 HTML 요소를 추가하고 싶지 않다면 Fragment를 사용할 수 있다.

```jsx
function App() {
  return (
    <>
      <h1>Hello</h1>
      <p>Welcome!</p>
    </>
  );
}
```

### 태그 닫기

JSX에서는 모든 태그를 닫아야 한다.

```jsx
<img src="image.png" />
<input type="text" />
```

## 3. JavaScript 표현식

중괄호 `{}`를 사용하면 JSX 안에 JavaScript 표현식을 넣을 수 있다.

```jsx
function App() {
  const name = "Yerin";
  const age = 16;

  return (
    <div>
      <h1>{name}</h1>
      <p>{age}살</p>
    </div>
  );
}
```

변수나 연산식 등을 중괄호 안에 작성할 수 있다.

```jsx
<p>{10 + 20}</p>
```

## 4. JSX와 HTML의 차이

JSX는 HTML과 비슷하지만 속성 작성 방식 등에 차이가 있다.

- `class` 대신 `className`을 사용한다.
- 이벤트 속성은 camelCase로 작성한다. 예: `onClick`
- JSX에서는 모든 태그를 닫아야 한다.
- 여러 요소를 반환할 때 하나의 부모 요소가 필요하다.

```jsx
function App() {
  return (
    <div className="container">
      <h1>Hello</h1>
    </div>
  );
}
```

## 5. 주석

JSX 안에서 주석을 작성할 때는 중괄호 안에 주석을 넣는다.

```jsx
function App() {
  return (
    <div>
      {/* JSX 주석 */}
      <h1>Hello</h1>
    </div>
  );
}
```

## 정리

- JSX는 JavaScript 안에서 HTML과 비슷한 문법을 작성하는 방식이다.
- JSX는 하나의 부모 요소로 감싸야 한다.
- 모든 태그를 닫아야 한다.
- `{}`를 사용하면 JavaScript 표현식을 넣을 수 있다.
- HTML과 JSX는 속성 작성 방식에 차이가 있다.
