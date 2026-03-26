# sales_order_facts

주문 단위의 매출/결제/환불/이행 상태를 저장한 운영 조회용 테이블

## Columns
- order_no: 주문번호
- order_date: 주문일자
- sales_channel: 판매 채널 (WEB, APP, PHONE)
- region: 지역 (SEOUL, BUSAN, DAEGU, GWANGJU, INCHEON, DAEJEON)
- product_category: 상품 카테고리
- product_name: 상품명
- quantity: 수량
- gross_amount: 할인 전 매출
- discount_amount: 할인 금액
- net_sales_amount: 순매출 금액
- payment_method: 결제수단
- payment_status: 결제 상태
- fulfillment_status: 주문 이행 상태
- refund_status: 환불 상태
- refunded_amount: 환불 금액
- promotion_code: 프로모션 코드
- is_membership_order: 멤버십 주문 여부

## Rules
- 매출은 net_sales_amount 기준
- 환불 금액은 refunded_amount 기준
- 주문번호가 있으면 단건 조회
- 기간 조건이 없으면 최근 7일 기본