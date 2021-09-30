# 자동 판매기 잔돈 계산 모듈

그저 반환되는 동전이 최소한이 되는 자판기 잔돈 계산 모듈을 구현해서 제공하면 충분하다.

- 최소 개수의 동전으로 잔돈을 돌려준다. <br>
예) 1000원 넣고 650원짜리 음료를 선택했다면, 잔돈은 100, 100, 100, 50원으로 반환한다.
<br><br>
- 지폐를 잔돈으로 반환하는 경우는 없다고 가정한다.

---
## 기능 요구 사항

- [x] 자판기에 동전을 넣으면 얼마가 들었는지 알 수 있다.
<br><br>
- [x] 자판기에 든 금액을 차감할 수 있다.
<br><br>
- [x] VendingMachine 이란 클래스 이름 다시 생각하기 (VendingMachine을 ChangeModule로 변경하기)
<br><br>
- [x] 동전은 500원, 100원, 50원, 10원이 있다.
<br><br>
- [x] 없는 금액의 동전인 경우 
<br><br>
- [x] 잔돈은 최소 개수의 동전으로 반환되어야 한다.
  - [x] 10원이 남아있다면 10원으로 돌려준다.
  - [x] 50원이 남아있다면 50원 동전 1개를 돌려준다.
  - [x] 1000원이 남아있다면 500원 동전 2개를 돌려준다.
  - [x] 20원이 남아있다면 10원 동전 2개를 돌려준다.
  - [x] 600원이 남아있다면 500원 동전 1개, 100원 동전 1개를 돌려준다.
  - [x] 650원이 남아있다면 500원 1개, 100원 1개, 50원 1개를 돌려준다.
  - [x] 잔돈을 거슬러 줄 수 없는 동전은 버리고, 거슬러 줄 수 있는 동전만 반환한다.
    - 예를들어 9원이 들어오면 아무것도 반환하지 않는다.
    - 624원이 들어오면 500원 1개, 100원 1개, 10원 2개를 반환하고 4원은 반환하지 않는다.
<br><br>
- [ ] 최소 구입 금액 이하인 경우 잔돈이 반환된다. (추후)
<br><br>
- [ ] 반환 요청을 받은 경우 잔돈이 반환된다. (추후)

---

- ChangeModule
  - ChangeModule#pop(Drink)
  - ChangeModule#withDraw(Money)
- Coin(500원, 100원, 50원, 10원)
- Changes(잔돈)