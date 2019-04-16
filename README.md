# 오프라인 코딩테스트 <영화 예매>

## 기능 요구사항
1. 영화 기본 정보로 아래의 항목이 주어진다.
    - 영화 아이디
    - 영화 제목
    - 요금
    - 상영 시작 시간
    - 상영 시간별 예매 가능 인원
2. 영화는 한번에 여러 영화를 예매할 수 있어야 한다.
    - 단, 일행이 각자의 취향에 따라 다른 영화를 예매한다고 가정한다.
    - 따라서 여러 영화를 예매할 경우 각 영화의 시작 시간 차이가 1시간 이상 차이가 날 수 없다.
3. 예매가 가능한 상태이면 결제를 진행한다.
4. 예매가 불가능한 경우 그 이유를 보여주고, 다시 예매할 수 있도록 해야 한다.
    - 상영 시작 시간이 이미 지난 영화를 선택하는 경우
    - 예매 가능 인원을 초과하는 경우
    - 두 영화의 시간 차이가 1시간 이내가 아닌 경우
    - 상영목록에 없는 영화를 선택한 경우
5. 결제 유형에 따라 할인율이 달라지고, 포인트를 사용할 수 있다.
    - 결제할 때 적립되어 있는 포인트를 사용할 수 있다.
    - 신용카드는 5%, 현금 결제는 2% 할인된다.
      할인은 포인트를 제외한 금액에 적용한다.
6. 최종 예매 금액을 보여준다.

## 기능 목록
- 예약할 영화 아이디를 입력받는다.
    - 아이디는 상영 영화 목록에 있는 숫자만 가능하며, 이외의 입력이 발생하면 다시 입력받는다.
- 적합한 영화 아이디가 입력되면 영화의 아이디, 제목, 요금을 출력한 후 상영 시작시간 및 예약가능인원을 출력한다.
- 예약할 시간표를 입력받는다.
    - 해당 영화의 시간표에서 적절한 것이 선택되어야 한다.
    - 시작시간이 지나지 않았는지, 예약가능인원이 남아 있는지 확인한다.
    - 적합하지 않으면 다시 입력받는다.
- 예약할 인원을 입력받는다.
    - 이미 입력받은 해당 시간표의 예약가능인원이 이번에 입력받은 예약할 인원을 수용 가능한지 확인한다.
    - 적합하지 않으면 다시 입력받는다.
- 예약을 종료하고 결제를 진행하려면 1번, 추가 예약을 진행하려면 2번을 입력받는다.
    - 1, 2가 아닌 입력이 발생하면 다시 입력받는다.
    - 1을 입력받으면 결제 단계로 넘어간다.
    - 2를 입력받으면 추가 예약을 진행한다.
- 결제 단계에서 포인트를 입력받는다.
    - 포인트는 최종 결제 금액을 넘을 수 없다.
- 신용카드는 1번, 현금은 2번을 입력받는다.
    - 이전 단계에서 포인트로 전액 결제를 한 경우 이 메뉴를 출력하지 않는다.
    - 1번을 선택한 경우 5%, 2번을 선택한 경우 2%를 할인한다. (포인트 사용 금액 제외)
- 최종 결제 금액을 출력한다.