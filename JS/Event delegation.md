# 이벤트 위임

이벤트 버블링과 캡처링을 이용한 것으로, 여러 요소에 각각의 이벤트 핸들러를 할당하는 것이 아닌 공통된 부모에 이벤트 핸들러를 할당하여 이벤트를 관리하는 방식이다. event.target을 사용하여 조상의 이벤트 핸들러에서 가장 처음 이벤트가 발생한 자식 요소를 가져올 수 있다.ㄹ