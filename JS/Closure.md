# 클로저

함수와 함수가 선언된 렉시컬 환경의 조합이다. 반환된 내부함수가 자신의 렉시컬 스코프를 기억하여 스코프 밖에서 호출되어도 그 스코프에 접근할 수 있는 함수를 의미한다. 클로저는 현재 상태를 기억하고 최신 상태를 유지해야 하는 상황에서 유용하다. 클로저가 없다면 상태를 유지하기 위해 전역 변수를 사용할 수 밖에 없고 이는 많은 부작용의 원인이 된다.