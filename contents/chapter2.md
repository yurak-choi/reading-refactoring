## 인상 깊었던 내용
- **누군가 "리팩터링하다가 코드가 깨져서 며칠이나 고생했다"라고 한다면, 십중팔구 리팩터링한 것이 아니다.**
- 리팩터링은 오로지 경제적인 이유로 하는 것이다.
  - 기능 추가 시간을 줄이고, 버그 수정 시간을 줄여준다.
  - 건드릴 일이 없거나 불편한 정도가 심하지 않으면 하지 않는다.
- 브랜치 통합 주기는 짧게 가져가는게 좋다.(CI/TBD)
  - 공감한다. 하지만 conflict 날 일이 없...ㅠ
- 간결한 설계, 점진적 설계, 에그니
  - 코딩 전에 아키텍처를 확정 지으려 하면 사전에 요구사항을 모두 파악해야 한다. 이는 불가능할 경우가 더 많다.
    - 기획이 완료 안 되어있는 경우
    - 기획이 바뀔 경우
    - 아직 모든 상황을 파악해서 설계할 능력도 안된다..
  - 현재 요구사항에 맞게 개발하면서 리팩터링을 통해 개발해 나간다.
    - 그렇다고 초기 설계를 소홀해서는 안된다.
- 대부분 프로그램은 전체 코드 중 극히 일부에서 대부분의 시간을 소비한다.
  - 성능 최적화에 돌입하기 전까지는 성능에 신경 쓰지 않고 코드를 다루기 쉽게 만드는 일에 집중한다.

## 느낀 점
- 평소 신규 기능 개발하면서 리팩터링(리팩터링인지.. 재구성인지..)을 같이 하는데 책에서도 수시로 하는게 좋다고 해서 기분이 좋았다.