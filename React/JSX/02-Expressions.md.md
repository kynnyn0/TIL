# JSX Expressions

## 1. JSX에서 JavaScript 사용하기

JSX에서는 중괄호 `{}`를 사용해서 JavaScript 표현식을 작성할 수 있다.

```jsx
function App() {
  const name = "Yerin";

  return <h1>Hello, {name}!</h1>;
}
```

중괄호 안에 변수를 넣으면 변수의 값이 화면에 표시된다.

## 2. 변수 사용하기

JavaScript에서 선언한 변수를 JSX 안에서 사용할 수 있다.

```jsx
function App() {
  const age = 16;
  const isStudent = true;

  return (
    <div>
      <p>나이: {age}</p>
      <p>학생 여부: {isStudent ? "학생" : "학생 아님"}</p>
    </div>
  );
}
```

## 3. 표현식과 연산

중괄호 안에서 숫자 계산이나 문자열 결합 등의 표현식을 사용할 수 있다.

```jsx
function App() {
  const price = 1000;
  const count = 3;

  return <p>총 가격: {price * count}원</p>;
}
```

```jsx
function App() {
  const firstName = "Yerin";
  const lastName = "Kim";

  return <h1>{lastName + " " + firstName}</h1>;
}
```

## 4. 조건부 표현식

삼항 연산자를 사용하면 조건에 따라 다른 값을 표시할 수 있다.

```jsx
function App() {
  const isLoggedIn = true;

  return (
    <h1>
      {isLoggedIn ? "환영합니다!" : "로그인해주세요."}
    </h1>
  );
}
```

- 조건이 `true`이면 `?` 뒤의 값이 표시된다.
- 조건이 `false`이면 `:` 뒤의 값이 표시된다.

## 5. 논리 AND 연산자

`&&`를 사용하면 조건이 참일 때만 JSX를 표시할 수 있다.

```jsx
function App() {
  const isAdmin = true;

  return (
    <div>
      {isAdmin && <p>관리자 메뉴</p>}
    </div>
  );
}
```

`isAdmin`이 `true`일 때만 `관리자 메뉴`가 표시된다.

## 6. JSX에서 사용할 수 없는 것

JSX의 중괄호 안에는 JavaScript 표현식을 작성할 수 있지만, 일반적인 문장(statement)을 직접 작성할 수는 없다.

```jsx
// 올바른 예
<p>{10 + 20}</p>
<p>{name}</p>
```

```jsx
// 올바르지 않은 예
<p>{if (true) { ... }}</p>
```

조건문을 사용해야 한다면 JSX 바깥에서 처리하거나 삼항 연산자 등을 사용할 수 있다.

## 정리

- `{}`를 사용하면 JSX 안에서 JavaScript 표현식을 사용할 수 있다.
- 변수와 연산식을 JSX에 넣을 수 있다.
- 삼항 연산자로 조건에 따라 다른 내용을 표시할 수 있다.
- `&&`를 사용하면 조건이 참일 때만 JSX를 표시할 수 있다.
- JSX의 중괄호 안에는 표현식을 작성한다.