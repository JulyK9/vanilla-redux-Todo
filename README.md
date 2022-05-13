# Vanilla Redux Todo

# 바닐라JS 와 redux의 조합으로 todo 구현

✔ MUTATE STATE 는 절대로 사용하지 말 것!
  - why???

📌 Redux 의 3가지 기본 원칙
  - 출처 : https://dobbit.github.io/redux/introduction/ThreePrinciples.html

😊 single source of truth 

😊 state 는 read-only
  - ex) store.getstate() + 1 (❌)
  - store 를 수정할 수 있는 유일한 방법은 action 을 보내는 방법뿐임

😊 변화는 순수 함수로 작성되어야 함
  - new state objects 를 리턴해야함 (mutating state 하는 대신)
  - 즉 상태를 수정하는 것이 아니라 새로운 object 를 리턴해야함

✔ 바닐라 자바스크립트에서 배열의 불변성을 유지하기 위한 방법
  - mutate 계열인 slice 함수를 쓰지 말 것
  - 새로운 배열을 생성하는 filter 함수를 사용할 것!
  - 원리 : 삭제하고싶은 object 를 제외시키고 새로운 배열을 다시 만들어 내는 것 => filter() 활용