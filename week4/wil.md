# Week 4 - Repository 계층과 JPA CRUD

## 이번 주 학습 키워드
- Repository 계층
- EntityManager
- JPA CRUD (Create, Read, Update, Delete)
- 영속성 컨텍스트
- 트랜잭션 (@Transactional)
- JPQL
- 테스트 코드와 @Rollback

## 배운 점
- Repository는 DB와 직접 소통하며 데이터를 저장, 조회, 수정, 삭제하는 계층이다.
- JPA의 EntityManager를 통해 `.persist()`, `.find()`, `.remove()` 등을 호출해 DB 조작이 가능하다.
- 영속성 컨텍스트는 1차 캐시 역할을 하며, 같은 ID의 객체는 동일 인스턴스로 유지된다.
- 트랜잭션 범위 내에서 데이터 변경 사항이 모이고, `commit` 시점에 일괄 반영된다.
- JPQL을 활용하면 SQL처럼 조건 조회가 가능하며, `:param` 형식으로 변수 바인딩을 한다.
- 테스트 시에는 `@Transactional`과 `@Rollback(false)`를 통해 실제 DB 반영 여부를 확인할 수 있다.

## 느낀 점
JPA의 작동 방식을 직접 실습하며, 추상화된 ORM이 어떻게 SQL을 대신 생성하고 DB와 소통하는지 이해할 수 있었다. 단순한 SQL보다 객체 중심의 사고가 가능해졌고, 영속성 컨텍스트 개념이 왜 중요한지도 체감되었다. 반복되는 CRUD 코드가 많아질수록 Spring Data JPA의 필요성도 느꼈다. 다음 주에는 이를 적용해 더 깔끔한 구조를 만들 수 있기를 기대한다.