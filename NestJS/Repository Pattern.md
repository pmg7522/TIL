## Directory Architecture

> NestJS의 기본적인 구조는 기능 별로 controller, module, service가 존재한다.

1. **Controller** <br> 클라이언트에서 요청을 받고 응답을 보내주는 역할을 한다.

2. **Module** <br> 애플리케이션 구조를 구성하는데 사용하는 메타 데이터를 제공하는 역할을 한다.

3. **Service** <br> 비즈니스 로직을 수행하며, Controller에 결과를 전달하는 역할을 한다.

**구조 예시**

```
src
 ┃ ┗ cats
 ┃ ┃ ┣ cats.controller.ts
 ┃ ┃ ┣ cats.module.ts
 ┃ ┃ ┗ cats.service.ts
```

---

## Repository Pattern

> 기존 구조에서 repository만 추가된 패턴이다.

1. **Controller** <br> 클라이언트에서 요청을 받고 응답을 보내주는 역할을 한다.

2. **Module** <br> 애플리케이션 구조를 구성하는데 사용하는 메타 데이터를 제공하는 역할을 한다.

3. **Service** <br> 비즈니스 로직을 수행하며, Controller에 결과를 전달하는 역할을 한다.

4. **Repository** <br> DB와 통신하는 로직을 수행하며, Service에 결과를 전달하는 역할을 한다.

**구조 예시**

```
src
 ┃ ┗ cats
 ┃ ┃ ┣ cats.controller.ts
 ┃ ┃ ┣ cats.module.ts
 ┃ ┃ ┣ cats.service.ts
 ┃ ┃ ┗ cats.repository.ts
```
