# 정규화 VS 비정규화

### 정규화

* 중복을 배제하여 삽입, 삭제, 갱신 이상의 발생을 방지
* 각 릴레이션에 중복된 종속성을 여러개의 릴레이션에 분할
* 어떠한 릴레이션이라도 데이터베이스 내에서 표현 가능하게 함
* 데이터 삽입 시 릴레이션을 재구성할 필요성 감소
* 효과적인 검색 알고리즘 생성 가능



### 하지만 중복된 데이터이면 반드시 정규화를 해야하는가?

정규화도 비용이다.

일기 비용을 지불하고 쓰기 비용을 줄이는것

****

### 정규화시 고려해야 하는것

* 얼마나 빠르게 데이터의 최신성을 보장해야 하는가.
* 히스토리성 데이터는 오히려 비정규화 하여야한다.
* 데이터 변경 주기와 조회 주기는 어떻게 되는가?
* 객체 탐색 깊이가 얼마나 깊은가



### 정규화를 하기로 했다면 읽기시 어떻게 데이터를 가져올 것인가?

조인은 테이블의 결합도를 엄청나게 높인다.

조회시에는 성능이 좋은 별도 데이터베이스나 캐싱등 다양한 기법을 이용

읽기 쿼리 한번 더 발생하는 것은 그렇게 큰 부담이 아닐 수 있다.


