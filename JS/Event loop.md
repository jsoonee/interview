# 이벤트 루프

태스크를 처리하는 자바스크립트 내의 루프를 의미한다. 기본적으로 자바스크립트는 싱글 스레드 언어로 동작하여 동시에 하나에 작업만을 처리할 수 있다. 여러 작업을 동시에 처리하기 위해 자바스크립트는 이벤트 루프라는 비동기 방식을 사용한다.

<br>

## 매크로태스크 큐 (Macrotask Queue)

외부 스크립트 로드, 이벤트 핸들러 실행, setTimeout의 콜백 함수 실행 등 JS 엔진이 처리하는 여러 태스크가 추가되는 큐를 말한다. 자바스크립트는 매크로태스크 큐 하나를 처리할 때마다 마이크로태스크 큐에 쌓인 마이크로태스크를 전부 처리한다.

<br>

## 마이크로태스크 (Microtask)

Promise 핸들러, then, catch, finally 등을 통해 비동기적으로 실행되는 태스크

<br>

## 이벤트 루프 알고리즘

1. 매크로태스크 큐에서 가장 오래된 태스크를 꺼내 실행한다.
2. 모든 마이크로태스크를 실행한다. 마이크로태스크 큐가 빌 때까지 오래된 순으로 처리한다.
3. 렌더링이 필요한 경우 렌더링한다.
4. 매크로태스크 큐가 비어있으면 새로운 매크로태스크가 나타날 때까지 대기한다.
5. 1번으로 돌아간다.
