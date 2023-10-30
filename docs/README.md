# 자동차 경주

## 기능 목록

- [x] 사용자로부터 자동차의 이름들을 입력받는다. - RaceController#askCarNames()
- [x] 입력받은 이름들을 쉼표(,)를 기준으로 구분한다.(이름 중복 허용) - RaceController#divideCarNames()
  - [x] 사용자로부터 입력받은 이름은 적어도 2개 이상을 입력받아야한다. 2개 이하의 이름을 입력 시 `IllegalArgumentException`을 발생시킨다. - InputValidator#validateCarNamesSize()
  - [x] 각 자동차 이름은 5글자 이하만 가능하다. 5글자를 초과한 이름이면 `IllegalArgumentException`을 발생시킨다. - InputValidator#validateCarNameLength()
- [x] 사용자로부터 이동을 시도할 횟수를 입력받는다. - RaceController#askMoveCount()
  - [x] 시도 횟수가 음수가 될 수 없으며 적어도 한 번 이상의 시도 횟수를 입력받아야 한다. 이 조건을 만족하지 않는 입력이면 `IllegalArgumentException`을 발생시킨다. - InputValidator#validateMoveCountRange()
- [x] 입력 받은 이름들을 각각 자동차에 부여하여 `List<Car>` 로 생성한다. - RaceController#createCars()
- [ ] 0에서 9사이의 무작위 값을 생성한다. - NumberGenerator#generateRandomNumber()
- [ ] 무작위 값이 전진 조건(4이상)을 만족하면 자동차는 위치를 +1 전진한다. - Car#moveForward()
- [ ] 자동차는 이동한 거리를 표현할 수 있다. - Car#expressMoveDistance()
- [ ] 자동차의 이동한 거리를 출력한다. - OutputView#showMoveDistance()
- [ ] 자동차는 서로 누가 더 앞서 있는지 알 수 있다. - Car#compareTo()
- [ ] 각 자동차들을 입력받은 시도 횟수만큼 전진 시도를 반복한다. - RaceService#repeatMoveCars()
- [ ] 각 자동차를 1회 전진 시도하고 결과를 볼 수 있다. - RaceService#tryMoveCars()
- [ ] 자동차 경주에서 어떤 차가 우승했는지 찾는다.(중복 우승 가능) - Referee#findWinners()
  - [ ] 가장 먼 위치에 있는 자동차를 찾는다. - Referee#findFarthestPositionCar()
  - [ ] 같은 위치에 있는 자동차를 찾는다. - Referee#findSamePositionCars()
- [ ] 자동차 경주 게임의 우승자를 출력한다. - OutputView#showWinners()
- [ ] 자동차 경주 게임의 정해진 프로세스에 따라 게임을 실행시킨다. - RaceController#run()

## 기능 요구 사항

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`을 발생시킨 후 애플리케이션은 종료되어야 한다.
