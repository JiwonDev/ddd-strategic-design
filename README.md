# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전
### 공통
| 한글명 | 영문명       | 설명                |
|-----|-----------|-------------------|
| 비속어 | profanity | 욕설,은어와 같은 부적절한 언어 |

### 음식
| 한글명   | 영문명           | 설명                           |
|-------|---------------|------------------------------|
| 음식    | product       | 음식 (ex) 등심돈까스, 안심돈까스, 치킨돈까스) |
| 음식 이름 | product name  | 음식의 이름 (비속어가 포함될 수 없음)       |
| 음식 가격 | product price | 음식의 가격 (0원 이상이어야 함)          |


### 메뉴 그룹
| 한글명      | 영문명             | 설명                        |
|----------|-----------------|---------------------------|
| 메뉴 그룹    | menu group      | 여러 메뉴들의 묶음 (ex) 등심돈까스 세트  |
| 메뉴 그룹 이름 | menu group name | 메뉴 그룹의 이름 (비속어가 포함될 수 없음) |


### 메뉴
| 한글명   | 영문명            | 설명                     |
|-------|----------------|------------------------|
| 메뉴    | menu           | 메뉴 음식들의 묶음 (ex) 돈까스 메뉴 |
| 메뉴 이름 | menu name      | 메뉴 이름 (비속어가 포함될 수 없음)  |
| 메뉴 가격 | menu price     | 메뉴 가격 (0원 이상이어야 함)     |
| 메뉴 음식 | menu product   | 메뉴를 구성하는 음식            |
| 메뉴 노출 | menu displayed | 메뉴 판매 상태               |


### 주문 테이블
| 한글명       | 영문명              | 설명                  |
|-----------|------------------|---------------------|
| 주문 테이블    | order table | 매장 식사시 손님이 이용하는 테이블 |
| 테이블 이름    | order table name | 주문 테이블 이름           |
| 손님 수      | number of guests | 테이블 손님의 수           |
| 테이블 사용 여부 | occupied table   | 테이블 사용 여부           |



### 주문
#### 공통
| 한글명   | 영문명            | 설명                                       |
|-------|----------------|------------------------------------------|
| 주문 타입 | order type     | 주문의 방식 (ex) 매장, 포장, 배달                   |
| 매장 주문 | eat-in order   | 매장 내에서 식사하는 주문                           |
| 포장 주문 | take-out order | 손님이 직접 음식을 찾으러 오는 주문                     |
| 배달 주문 | delivery order | 배달 업체를 통해 배달되는 주문                        |
| 주문 상태 | order status   | 주문의 상태 (ex) 접수중, 접수완료, 서빙완료, 배달중, 배달완료, 완료 |
| 접수중   | waiting        | 주문 접수가 진행 중인 상태                          |
| 접수 완료 | accepted       | 주방에 주문이 들어간 상태                           |
| 서빙 완료 | served         | 접수된 주문이 조리가 완료된 상태                       |
| 배달 중  | delivering     | 조리가 완료된 음식을 배달업체에서 배달 중인 상태              |
| 배달 완료 | delivered      | 손님에게 배달이 완료된 상태                          |
| 완료    | completed      | 각 주문의 상태가 모두 완료된 상태                      |
| 주문 시간 | order Date     | 주문을 한 시간                                 |


#### 매장 주문 
| 한글명  | 영문명            | 설명                              |
|------|----------------|---------------------------------|
| 주문 타입 | order type     | eat-in                          |
| 접수중  | waiting     | 손님이 주문 후, 매장에서 주문을 접수처리 전 상태    |
| 접수 완료 | accepted    | 매장에서 주문이 완료되어 주방에 주문이 들어간 상태    |
| 서빙 완료 | served      | 접수된 주문이 조리 되어 매장 내 손님에게 전달 된 상태 |
| 주문 완료 | completed   | 손님이 음식을 다 먹고 주문 테이블 정리가 된 상태    |
#### 포장 주문
| 한글명   | 영문명            | 설명                           |
|-------|----------------|------------------------------|
| 주문 타입 | order type     | take-out                     |
| 접수중  | waiting        | 손님이 주문 후, 매장에서 주문을 접수처리 전 상태 |
| 접수 완료  | accepted       | 매장에서 주문이 완료되어 주방에 주문이 들어간 상태 |
| 서빙 완료  | served         | 접수된 주문이 조리 완료된 상태            |
| 주문 완료   | completed     | 손님이 음식을 가져간 후 주문이 종료가 된 상태   |
#### 배달 주문
| 한글명   | 영문명              | 설명                               |
|-------|------------------|----------------------------------|
| 주문 타입 | order type       | delivery                         |
| 배달 주소 | delivery address | 배달의 목적지 주소                       |
| 배달 업체 | delivery company | 배달 대행 업체                         |
| 접수중 | waiting          | 손님이 주문 후, 매장에서 주문을 접수처리 전 상태     |
| 접수 완료 | accepted         | 매장에서 주문이 완료되어 주방에 주문이 들어간 상태     |
| 음식 완료 | served           | 접수된 주문이 조리 완료된 상태                |
| 배달 시작 | delivering       | 배달이 시작되어 진행중인 상태                 |
| 배달 완료 | delivered        | 배달이 완료된 상태                       |
| 주문 완료 | completed        | 손님에게 배달이 완료된 후 주문이 종료가 된 상태 |




## 모델링
