# DB-cloud

# Cloud에서 쓸수 있는 DB??????
![image](https://user-images.githubusercontent.com/75401920/112100536-a0b7b680-8be8-11eb-8f13-ebaa392dd984.png)


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
  
     -가장 기본적인 NoSQL
     
     -Redis, [DynamoDB](https://pjh3749.tistory.com/282)

 ii. Column family store

     -row기반의 RDBMS와 달리 column기반으로 데이터를 저장
     
     -Casandra, HBase
     
 iii. Document store

     -json, xml형식의 문서와 같은 반정형 데이터 저장을 위한 모델
     
     -mongoDB, CouchDB
  
 iv. Graph store
  
     -그래프로 표현하는 DB
     
     -Neo4J
 

# SQL VS NOSQL
![image](https://user-images.githubusercontent.com/75401920/112100183-12dbcb80-8be8-11eb-93bc-da1cb1be408a.png)
