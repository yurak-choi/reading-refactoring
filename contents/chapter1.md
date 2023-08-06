## 인상 깊었던 내용
- 코드 전체를 파악하고 리팩터링 하는 것이 아니라 특정 부분을 함수로 빼면서 리팩터링을 실행할 수 있다.
- 반복문 쪼개기
    - 같은 반복 범위를 가지더라도 관심사에 따라 분리할 수 있다.
```
// AS-IS
let totalAmount = 0;
let volumeCredits = 0;
let result = `청구 내역 (고객명: ${invoice.customer})\n`;

for (let perf of invoice.performances) {
  volumeCredits += volumeCreditsFor(perf);

  result += ` ${playFor(perf).name}: ${usd(amountFor(perf))} . (${perf.audience}석)\n`;
  totalAmount += amountFor(perf);
}

// TO-BE
let totalAmount = 0;
let result = `청구 내역 (고객명: ${invoice.customer})\n`;

for (let perf of invoice.performances) {
  result += ` ${playFor(perf).name}: ${usd(amountFor(perf))} . (${perf.audience}석)\n`;
  totalAmount += amountFor(perf);
}

let volumeCredits = 0;
for (let perf of invoice.performances) {
  volumeCredits += volumeCreditsFor(perf);
}
```

- 변수명 짓기
    - 변수명을 지을 때 무슨 의미인지 알 수 있도록 지으라고 해서 모든 곳에 의미를 담은 변수명을 지으려고 노력을 해왔다. 하지만 책에서는 변수를 리턴을 하는 함수에서 리턴 변수명을 간단하게 result로 지었다. 모든 곳에 변수명을 의미있게 지을려고 고민할 필요는 없을 것 같다.
 ```
// AS-IS
function totalAmount() {
  let totalAmount = 0;
  for (let perf of invoice.performances) {
    totalAmount += amountFor(perf);
  }
  return totalAmount;
{

// TO-BE
function totalAmount() {
  let result = 0;
  for (let perf of invoice.performances) {
    result += amountFor(perf);
  }
  return result;
{
```
- 테스트
    - 개인적으로 테스트 코드 작성은 많이 귀찮다… 하지만 리팩터링할 때 테스트는 중요하다는 생각이 들었다.

## 정리
책에서는 매우 작은 단위로 쪼개면서 리팩터링을 하였다. 리팩터링을 하는 이유가 가독성 및 수정에 용이하기 위한 것인데 이때까지 실제 업무에서 수정을 한다고 하면 작은 기능 변경이 아니라 무엇인가가 사라지고 생기고 하는 단위의 수정이 대부분이었다. 그래서 실무에서는 책에 나온만큼의 단위로 쪼개는건 '오히려 낭비가 아닐까?' 라는 생각이 든다. 특정 기능을 하는 라이브러리 같은 것을 개발하게 된다면 책에서의 작은 단위로 쪼개서 개발하면 좋을 것 같다.


