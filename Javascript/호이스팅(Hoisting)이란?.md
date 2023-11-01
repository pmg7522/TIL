## 호이스팅(Hoisting)

자바스크립트 호이스팅은 인터프리터가 코드를 실행하기 전에 함수, 변수, 클래스 또는 import의 선언문을 해당 범위의 맨 위로 이동시키는 과정을 말합니다.

### 변수 호이스팅

변수

```js
console.log(a); // undefined

var a;

console.log(a); // undefined

a = 1;

console.log(a); // 1
```

위와 같이 `a`를 `console.log(a)`를 실행하고난 후에 선언한 것처럼 되어있어 에러가 나야될 것 처럼 보이지만, 호이스팅으로 인해 위로 끌어 올려져 실제 코드 동작 순서는 아래와 같이 동작합니다.

```js
var a;

console.log(a); // undefined

console.log(a); // undefined

a = 1;

console.log(a); // 1
```

### 함수 호이스팅

```js

```
