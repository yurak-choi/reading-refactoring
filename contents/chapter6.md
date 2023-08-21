## 인상 깊었던 내용

- 함수 선언 바꾸기 - 마이그레이션 절차
  - 기존에 사용하고 있는 함수를 수정할 때 한번에 변경하면 테스트 부담이 있는데 해당 방법을 사용하면 안전하게 변경할 수 있어서 좋았다.
```
// AS-IS
function circum(radius) {
  return 2 * Math.PI * radius;
}

// TO-BE
function circum(radius) {
  return circumference(radius)
}

function circumference(radius) {
  return 2 * Math.PI * radius;
}
```
- 이름 앞에 타입이 드러나는 문자 붙이기
  - ex) 매개변수: aCustomer
- 객체 지향 프로그래밍
  - 객체 지향 프로그래밍이 공통 관심사를 묶어서 코드를 이해하기 쉽게 도와주는 것은 공감한다.
  - 하지만 객체를 설계하는 것이 어렵다.
  - 그리고 자바스크립트에서 객체 지향.. 잘 모르겠다.

### 느낀 점
- 리팩터링은 가독성을 기반으로 한 네이밍이 핵심인 것 같다. 이를 기반으로 상황에 따라 함수/변수 추출, 함수/변수 인라인을 사용하는데 각각 사용할 상황이 책의 예시는 구분이 갔지만 실제 적용할 때 애매한 부분이 많을 것 같다.
