# bot database 종류

1. daily_craw: 종목별 일별 금융 거래 데이터를 저장하는 데이터베이스
2. main_craw: 종목별 분별 검융 거래 데이터를 저장하는 데이터베이스
3. daily_buy_list
    1. 일자 별로 상장된 모든 종목들의 금융 데이터를 저장
    2. 주식 종목 리스트 저장
    3. 테이블 종류
        1. stock_item_all: 코스피, 코스닥, 코넥스의 모든 종목을 저장하는 테이블
        2. stock_kospi: 코스피 종목 리스트
        3. stock_kosdaq: 코스닥 종목 리스트
4. jackbot1_imi1
    1. 모의투자 데이터베이스
    2. 테이블 종류
        1. all_item_db: 종목 거래 이력 테이블
        2. jango_data: 일별 수익률 정산 테이블
        3. possessed_item: 현재 보유 중인 종목 리스트 테이블
        4. setting_data: 봇 옵션 관리 및 DB 업데이트 일자 관리 테이블

## 초기 database 생성 쿼리문

-   `collector_v1.py`를 실행시키면 자동으로 아래 DB가 없을시 생성되도록 코드 수정

```sql
CREATE DATABASE daily_craw;
CREATE DATABASE min_craw;
CREATE DATABASE daily_buy_list;
```
