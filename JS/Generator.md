# 제너레이터

일반 함수에서 값을 반환할 경우 하나의 값만을 반환할 수 있지만, 제너레이터를 활용하면 여러 개의 값을 필요에 따라 하나씩 반환할 수 있다.

<br>

## 제너레이터 함수

function\* 키워드(끝에 별표가 있는 function 키워드)로 선언하며, 제너레이터 객체를 반환한다.

<br>

## 제너레이터 객체

제너레이터 함수의 반환값으로, 이터러블 프로토콜과 이터레이터 프로토콜을 따르는 객체이다. 이때, 제너레이터의 이터러블에서 반환되는 이터레이터는 자기 자신이다.

<br>

## yield와 return

- yield : 제너레이터 함수의 실행을 일시적으로 중지시키고, yield 뒤에는 제너레이터 프로토콜을 통해 반환할 값의 표현식을 정의한다.
- yield\* : 다른 제너레이터 함수가 위임되어 진행된다.
- return : 제너레이터 함수 안에서의 return은 수행중인 이터레이터를 종료시키며, return 뒤의 값은 이터레이터 객체의 value 프로퍼티에 할당되며, done 프로퍼티에는 true가 할당된다.

<br>

## next 메소드

제너레이터 객체의 메소드로, 호출될 때마다 제너레이터 함수가 실행을 재개한다. next가 호출되면 가장 가까운 yield 문을 만날 때까지 실행이 지속되어 value와 done 프로퍼티를 가진 객체를 반환한다.

<br>

## return 메소드

일반적인 상황에서 { done: true, value: 값 } 형태의 객체를 반환한다. 즉 제너레이터를 종료하는 메소드이다. 하지만 return 메소드 호출 시 제너레이터 함수의 코드가 try...finally 구문 안에 있으면 제너레이터가 종료되지 않는다. return 이후 finally 블록의 yield 표현식이 실행되며, 시퀀스는 return 메소드에 전달된 값으로 종료된다.

<br>

## throw 메소드

- 현재 중단된 위치에서 제너레이터에 throw 문이 삽입되는 것처럼 작동하여 제너레이터의 오류 조건을 알려주고 오류를 처리하거나 정리 작업을 수행하며 제너레이터를 종료할 수 있도록 한다.
- throw 호출 시 try...catch 구문의 catch 블록에 throw 인자가 전달된다. 해당 에러는 catch 블록 안의 yield 문으로 던져진다.
