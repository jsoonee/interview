# async와 await

비동기식 Promise 동작을 더욱 편하게 사용할 수 있도록 한 문법이다.

<br>

## async 함수

Promise 객체를 반환하는 비동기 함수이다.

<br>

## await

Promise가 처리될 때까지 기다리고, 결과를 반환하도록 하는 키워드이다. 에러가 발생할 경우 throw 문을 작성한 것처럼 에러가 던져지고, 에러가 발생하지 않으면 Promise 객체의 result에 저장된 값을 반환한다.
