**8.1 함수 옮기기**
- 좋은 소프트웨어 설계의 핵심은 모듈성(모듈화가 얼마나 잘 되어 있느냐) 이다.
- 모듈성을 높이려면 서로 연관된 요소들을 묶고 요소 사이의 연결 관계를 쉽게 찾고 이해할 수 있어야 한다.
    - 시간이 지날수록 이해도가 높아지므로 요소들을 이리저리 옮겨야 할 수 있다.

**8.2 필드 옮기기**
- 어떤 상황에서 사용하는지 어떤걸 설명하고 싶은지 이해를 못했다..

**8.3 문장을 함수로 옮기기**
- 특정 함수를 호출하는 코드가 나올 때마다 그 앞이나 뒤에서 똑같은 코드가 추가로 실행되면 함수로 합친다.
    - 어떤 상황을 말하는걸까.. 저렇게 코드를 구현하는 사람이 있을까??

**8.4 문장을 호출한 곳으로 옮기기**
- 추상화라는 것이 그 경계를 항상 올바르게 긋기가 만만치 않다.
    - 그래서 어쩔때는 너무 나눠서 개발하고 어쩔때는 합쳐서 개발한다
    - 8.3과 8.4를 적절히 사용하며서 리팩터링을 해나가야할것 같다

**8.5 인라인 코드를 함수 호출로 바꾸기**
- 이미 존재하는 함수와 같은 일을 하는 인라인 코드가 있으면 함수 호출로 대체한다

**8.6 문장 슬라이드하기**
- 관련된 코드들이 가까이 모여 있다면 이해하기 쉽다.
- 모든 변수를 함수 첫마리에 선언 vs 변수를 처음 사용할 때 선언
    - 섞어서 사용하지만 전자를 더 많이 하는 것 같다.
    - 전자를 사용하면서 코드 읽기가 힘들어지면 코드를 나누려고 한다(시간이 있다면…)
- 명령-질의 분리 원칙 나중에 찾아보기

**8.7 반복문 쪼개기**
- 반복문 하나에서 두 가지 일을 하면 수정할 때 두 가지 일 모두 잘 동작하는지 계속 확인해야 한다. 반복문을 분리하면 수정할 동작 하나만 이해하면 된다.
- 리팩터링과 최적화를 구분하자. 반복문 쪼개기가 병목으로 이어지면 다시 합치면 된다.

**8.8 반복문을 파이프라인으로 바꾸기**
- 뻔한 이야기

**8.9 죽은 코드 제거하기**
- 버전 관리 시스템이 있다
- 어느 리비전에서 삭제했는지를 커밋 메시지로 남겨놓자
- 마지막으로 이렇게 했던게 언제인지 기억도 나지 않으며 후회한 기억도 없다.
