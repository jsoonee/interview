# Promise

비동기 작업이 맞이할 미래의 완료 또는 실패와 그 결과값을 나타내는 객체로, 주로 서버에서 받아온 데이터를 표시할 때 사용한다.

<br>

## Promise의 세 가지 상태

- Pending(대기) : 비동기 처리 로직이 아직 완료되지 않은 상태이다. Promise 생성자를 호출할 때 Pending 상태가 된다.
- Fullfilled(이행) : 비동기 처리가 완료되어 Promise가 결과값을 반환해준 상태이다. Promise 생성자의 콜백 함수의 인자 resolve가 실행되었을 때 Fullfilled 상태가 된다.
- Rejected(실패) : 비동기 처리가 실패하거나 오류가 발생한 상태이다. Promise 생성자의 콜백 함수의 인자 reject를 호출할 시 Rejected 상태가 되며 catch 메소드를 통해 에러값을 받을 수 있다.
