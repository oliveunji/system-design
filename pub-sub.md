# Pub-sub 이란?
Pub Sub 방식의 비동기 서비스간 커뮤니케이션 방식
서버리스와 마이크로 서비스 아키텍쳐에서 주로 사용된다. 

## Pub-sub의 Use cases
1. Improve Performance - push기반의 배포가 가능하기 때문에 받는 쪽에서 주기적으로 polling 필요없다
1. Handling Ingestion - 중간에 버퍼 역할을 하기 때문에 log ingestion등의 많은 양의 데이터 ingestion에 유리
1. Real-time monitoring - 리얼타임 시스템 모니터링에 사용됨
1. Replicating Data - multiple view가 가능하다. 

- Q. Queue와 pub sub의 차이?
큐는 Consumer가 1명이라면 pub-sub 구조는 consumer 여러명이 가능하다 

# Pub sub 설계하기
## 기능 요구사항 
- 토픽생성
- 구독 기능
- 메세지 작성
- 메세지 읽기
- retention time 정하기
- 메세지 삭제 (retention 지난 메세지들)

## 비기능 요구사항
- 가용성 (Availability) - 언제든 producer가 데이터 추가하고, consumer가 추가될 수 있어야 한다. 
- 내구성 (Fault tolerant) - 한 컴포넌트에 장애가 발생해도 다른 컴포넌트들이 영향받으면 안된다. 
- 동시성 (Concurrent) - 읽기 쓰기가 동시에 이뤄져도 처리 가능해야 한다. 
- 확장성 (Scalabiltiy) - 토픽의 갯수가 증가하고 쓰기 연산이 증가해도, Scalable 해야한다. 
- Duravitiy - 받은 메세지 분식하면 안된다. 

## API 설계
TBD

## Pub sub 설계하기 위해 필요한 구성요소 나열 및 설명
TBD


