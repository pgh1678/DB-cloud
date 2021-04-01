# DB-cloud

# Cloud에서 쓸수 있는 DB??????
![image](https://user-images.githubusercontent.com/75401920/112100536-a0b7b680-8be8-11eb-8f13-ebaa392dd984.png)


# AWS RDS 6종



1. Amazon Aurora:

   – Aurora는 MySQL RDBMS로 클라우드 기반의 RDBMS
   
   – Aurora는 사용량이 증가함에 따라 10GB씩 최대 64TB까지 자동으로 확장됨
   
   – 데이터베이스의 성능은 용량에 따라 일정하게 증가하며, 더 높은 IOPS가 필요할 경우 순간적인 확장이 가능
   
   – 높은 가용성을 보장하기 위해 3곳의 가용 영역(AZ)에 데이터 복제본을 2개씩 자동으로 생성
   
   – 이러한 이중화 덕분에 6개의 복제본 중 4개만 쓰기(write)가 완료되어도 즉시 데이터를 처리 가능
   
   – Aurora DB는 최대 15개의 복제본을 생성 할 수 있으며, 10 ~ 20 밀리세컨드(만분의 1초) 단위의 페일오버(Failover) 조치가 가능

2. MySQL:
   
   – 사용자는 설치하는 동안 5.5, 5.6 및 5.7의 MySQL 버전과 각각의 마이너 버전을 구성 가능
   
   – Amazon은 RDS를 처음 출시한 후 최소 3년 동안 각 버전들을 지원 가능
   
   – Aurora와 달리 MySQL 인스턴스는 오토스케일링(Auto-scaling)이 불가능하고 여러 가용영역(AZ)에 복제될 수 없습니다.
   
   – 사용된 데이터베이스에 대해서만 비용을 지불하는 Aurora와 달리, MySQL은 스토리지에 대한 비용을 지불해야 함.
   
   – 장점으로는 MySQL의 확장성을 꼽을 수 있음.
   
   – Aurora는 가장 작은 인스턴스가 t2.small인 반면 MySQL은 그보다 작은 t2.micro 인스턴스 단위까지 프로비저닝 가능.

3. MariaDB:

   – MariaDB는 MySQL의 한 갈래에 속하는 DB로 자동 패치 및 데이터베이스 스냅 샷을 포함하여 RDS MySQL 서비스와 유사한 기능을 제공.
   
   – 인스턴스는 마그네틱, 범용 SSD을 제공하고, 높은 IOPS가 예상되는 경우 인스턴스당 1,000에서 30,000 IOPS까지 지원하는 SSD Elastic Block Store Storage를 사용 가능.
   
   – 사용자는 페일오버(failover) 기능을 사용하여 가용영역(AZ) 전체에 인스턴스를 자동으로 복제 가능.

4. Oracle:

   – 엔터프라이즈 기업들이 대부분 사용하고 있는 Oracle 데이터베이스는 RDS 내에서 온-디멘드(즉시주문) 또는 리저브드(Reserved, 예약) 로 할당 가능.
   
   – EC2 인스턴스와 마찬가지로 리저브드 데이터베이스는 조건에 따라 시간당 20%~60% 할인된 요금으로 선 지불 가능.
   
   – 오라클라이센스 보유 여부에 따라 별도 가격 정책.

5. Microsoft SQL Server:

   – Windows 데이터베이스의 표준 인스턴스로 Amazon RDS는 SQL Server 2008 R2, 2012/2014 Express, 2008 Standard/Enterprise, 2012 Enterprise를 지원.
   
   – 리저브드 인스턴스에 대해 할인이 적용되며, 이 중 Microsoft Software Assurance를 보유한 기업은 자체 라이선스를 적용해 큰 할인율을 적용 받을 수 있음.

6. PostgreSQL:

   – 여타 오픈 소스 데이터베이스와 동일한 가격으로 핵심 관리 및 패치 기능이 제공됨
   
   – PostgreSQL은 RDS로 이전 시 기존 어플리케이션 코드를 많이 변경하지 않아도 되기 때기 때문에 지리정보 분석, 머신러닝 등의 시스템 개발자에게 인기가 높음.


# AWS기준 DB별 가격 비교

![image](https://user-images.githubusercontent.com/75401920/112788108-10b8b780-9095-11eb-822b-31276591531c.png)


# NOSQL ?????
 
1. Not Only SQL
 
 RDBSM와는 뭔가가 다름.........=> 데이터를 저장하는 형태가
 
 ![image](https://user-images.githubusercontent.com/75401920/112103302-e7a7ab00-8bec-11eb-9941-4d89b41142d5.png)

 ![image](https://user-images.githubusercontent.com/75401920/112103382-00b05c00-8bed-11eb-98c8-ae525aac6eed.png)
 
  - 비관계 : 외래키 등으로 데이터 간의 관계를 제약하지 않음
  - 조인불가 : 일반적으로 테이블간 조인 연산 불가
  - 스키마 유연 : 데이터 저장 컬럼은 각기 다른 이름과 다른 타입이 허용됨

    => 고정된 스키마가 없고, 수평적 확장이 쉬움. 고가용성
 
2. 종류

 i. key-value store
  
   - 가장 기본적인 NoSQL     
   - Redis, [DynamoDb](https://pjh3749.tistory.com/282)

 ii. Column family store

   - row기반의 RDBMS와 달리 column기반으로 데이터를 저장   
   - Casandra, HBase
     
 iii. Document store

     -json, xml형식의 문서와 같은 반정형 데이터 저장을 위한 모델
     
     -mongoDB, CouchDB
  
 iv. Graph store
  
     -그래프로 표현하는 DB
     
     -Neo4J
 

# SQL VS NOSQL

![image](https://user-images.githubusercontent.com/75401920/113251962-20870480-92fe-11eb-85f2-3a5192ba123b.png)

![image](https://user-images.githubusercontent.com/75401920/112100183-12dbcb80-8be8-11eb-93bc-da1cb1be408a.png)
