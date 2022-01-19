# 자동차 경주 게임

## 기능 목록
- [X] 각 자동차의 이름을 입력받는다. InputView#getCarNames()
  - [X] 자동차의 이름은 쉼표(,)를 기준으로 구분한다. StringUtils#splitCarNames()
  - [X] 각 자동차의 이름은 5자 이하여야 한다. Name#validateLength()
- [X] 경주를 진행할 횟수(라운드)를 입력받는다. InputView#getRound()
  - [X] 경주를 진행할 횟수는 1 이상의 정수여야 한다. Round#validateRound()
- [ ] 각 자동차별로 전진 혹은 멈춤을 한다. Car#isMovable()
  - [ ] 각 자동차 별로 0~9 사이 무작위 정수를 생성하고, 값이 4 이상일 경우 전진한다. Car#move() 
  - [ ] 매 라운드가 끝나면 자동차의 이름과 위치를 "-" 기호를 통해 출력한다. OutputView#printResult()
- [ ] 경주가 끝나면 우승자를 출력한다. OutputView#printWinner()
  - [ ] 경주가 끝났을 때 위치값이 가장 큰 자동차의 이름을 출력한다. RacingGame#findWinner()
  
## 기능 요구 사항
- [ ] 초간단 자동차 경주 게임을 구현한다.
- [ ] 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- [ ] 각 자동차에 이름을 부여할 수 있다. 자동차 이름은 5자를 초과할 수 없다.
- [ ] 자동차 이름은 쉼표(,)를 기준으로 구분한다.
- [ ] 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- [ ] 사용자는 몇 대의 자동차로 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- [ ] 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- [ ] 자동차의 상태를 화면에 출력한다. 어느 시점에 출력할 것인지에 대한 제약은 없다.
- [ ] 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.

##추가된 요구 사항
- 모든 로직에 단위 테스트를 구현한다. 단, UI(System.out, System.in) 로직은 제외
- indent(인덴트, 들여쓰기) depth를 2를 넘지 않도록 구현한다. 1까지만 허용한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메서드)를 분리하면 된다.
- else 예약어를 쓰지 않는다.
  - else 예약어를 쓰지 말라고 하니 switch/case로 구현하는 경우가 있는데 switch/case도 허용하지 않는다.
  - 힌트: if문에서 값을 반환하는 방식으로 구현하면 else 예약어를 사용하지 않아도 된다.
- 함수(또는 메서드)의 길이가 15라인을 넘어가지 않도록 구현한다.
  - 함수(또는 메소드)가 한 가지 일만 하도록 최대한 작게 만들어라.

# 문자열 계산기
## 기능 목록
- [ ] 문자열의 사칙연산을 수행한다. calculator.domain.Calculator#calculate()
  - [X] 문자열은 공백을 기준으로 분리한다. StringUtils#splitExpression()
  - [X] 빈 문자열 혹 올바른 사칙연산 문자열만 들어올 수 있다. calculator.domain.Calculator#validateIdleExpression()
  - [X] 문자열에는 숫자와 사칙연산 기호만 들어올 수 있다. calculator.domain.Calculator#validateOperand()
- [X] 사칙연산은 덧셈, 뺄셈, 나눗셈, 곱셈이 가능하다 calculator.domain.Calculator#validateQuery()
    - [X] 사칙연산의 우선순위는 무시된다.
- [ ] 사칙연산의 결과를 출력한다. ResultView#result()

## 기능 요구 사항
- [ ] 사용자가 입력한 문자열 값에 따라 사칙 연산을 수행할 수 있는 계산기를 구현해야 한다.
- [X] 문자열 계산기는 사칙 연산의 계산 우선순위가 아닌 입력 값에 따라 계산 순서가 결정된다. 즉, 수학에서는 곱셈, 나눗셈이 덧셈, 뺄셈 보다 먼저 계산해야 하지만 이를 무시한다.
- [X] 예를 들어 "2 + 3 * 4 / 2"와 같은 문자열을 입력할 경우 2 + 3 * 4 / 2 실행 결과인 10을 출력해야 한다.