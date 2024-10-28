# ◈ 구현목표
![목표시스템의 역할 JPG](https://github.com/user-attachments/assets/ec1fe4d6-0a9e-4e25-bf32-aa599ba0d684)

![계산식구상기본개념](https://github.com/user-attachments/assets/bcabb27b-5abc-4116-b44a-9696b63bb5b3)

# ◈ Tableau Prepbuilder
### ■ 요약
- Tableau Desktop 대시보드 구성 전 데이터 전처리
- 정보시스템에서 생산된 원천(RAW) 데이터 소스 조인, 유니온, 계산식 통해 연산에 적합한 데이터구조 마련

![01 Prep Overview](https://github.com/user-attachments/assets/79ee4875-9709-4e86-8cdb-1afb6e0adfb2)
- 계약시작일, 계약종료일 등 계약정보 내 필드항목 기반 매출정보 추정 데이터 전처리 프로세스 구축

### ■ 신규/갱신 사업분류별 년월별 일수계산 개념도
![일수계산개념도](https://github.com/user-attachments/assets/47d759ff-46b6-41b3-8edc-b3df2051370e)

### ■ 계약기간 기준일별 년월별 매출일수계산 개념도
![기간별 계산식 적용개념도](https://github.com/user-attachments/assets/4745325e-a4b1-47dc-96e6-8cf29ae2ea11)

![기간별 계산식 적용개념도2](https://github.com/user-attachments/assets/e92d6e82-fb2a-422f-8c19-12163ce99f3c)

- 위 경우의 수 적용한 IF구문 전문 'tableau-calculation/01.prepbuilder/년월별일수계산' 소스첨부

### ■ Prepbuilder 계산식 적용결과
![Prep 데이터전처리(비표)](https://github.com/user-attachments/assets/a7b3cc9f-735e-4f88-b840-1b2e9f9378bb)
- 계약기간(시작/종료)을 통해 일수 산출 후 계약금액 기초데이터 기반 일별매출 산출
- [년월별 해당일수 * 일별매출 = 년월별매출] 산출된 결과를 (.hyper) 출력하여 Tableau Desktop 시각화

# ◈ Tableau DeskTop
### ■ 요약
- 데이터 테이블 조인, 필드간 계산식을 통해 목표 데이터 추출/대시보드 구축
- 다양한 필드(부서,담당,요율,금액 TopN, 사업분류 등) 조건 별 하이라이트 및 필터적용
- 수주현황/매출현황/잔여현황 대시보드 계산식 전문 'tableau-calculation/02.Desktop/계산된필드' 소스첨부

### * 계약(수주) 현황 대시보드
![수주현황(비표)](https://github.com/user-attachments/assets/a2d33654-e7a3-4bea-9b82-1098b608f506)
#### 주요지표
- 부서/담당별 계약현황(비율/금액) 및 월별수주추이
- 예년대비수주액, 잔여수주액, 목표달성율, 평균월매출, 수주요율 상관관계

### * 매출현황 대시보드
![매출현황(비표)](https://github.com/user-attachments/assets/32b17918-1e9d-4262-85f0-52b2a766d9af)
#### 주요지표
- 최근 3-5개년 매출추이, 미래 순환매출추정, 부서별 매출비율, 수주/매출상관관계, 예상평균월매출

### * 잔여현황 대시보드
![잔여현황(비표)](https://github.com/user-attachments/assets/4e909726-5229-49e1-bcfd-4ec647be3095)
#### 주요지표
- 부서/담당별 잔여계약현황, 각 월별 잔여계약현황, 계약목록 상태값(지연/정상/미도래) 노출
- 잔여건수, 잔여수주액, 목표수주액, 목표달성율, 계약금액 Top N

#### - 끝 -
