김영한님의 [스프링 DB 1편 - 데이터 접근 핵심 원리](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-db-1/dashboard?cid=328723) 실습 코드 아카이브

---

### 💻 Development Environment

* Java 21
* Spring Boot 4.0.2
* Gradle
* IDE: IntelliJ
* H2 database 2.2.4.240

### 🏆 실습 목표

* JDBC의 등장 배경과 원리를 이해하고, 순수 JDBC 코드로 데이터베이스 CRUD를 직접 구현
* 커넥션 풀(Connection Pool)과 데이터소스(DataSource)의 개념을 익히고 실무적인 연결 방식 습득
* 트랜잭션의 동작 원리(ACID, 락)를 DB 레벨에서 이해하고, 스프링이 제공하는 트랜잭션 추상화 기술 적용
* 자바 예외 계층과 실무 예외 처리 전략을 학습하며, 스프링의 예외 추상화와 JdbcTemplate을 통해 반복 코드 제거

### 📝 Curriculum

1. [**JDBC 이해**](https://mxxikr.github.io/posts/spring-db-jdbc-basics/)
    * JDBC 표준 인터페이스의 이해와 H2 데이터베이스 설정
    * `DriverManager`를 이용한 데이터베이스 연결 획득 및 CRUD(등록, 조회, 수정, 삭제) 기능 개발


2. [**커넥션풀과 데이터소스 이해**](https://mxxikr.github.io/posts/spring-db-connection-pool-datasource/)
    * 커넥션 풀(Connection Pool)의 개념과 사용하는 이유 이해
    * `DataSource` 인터페이스를 통한 커넥션 획득 방법 추상화 및 `HikariCP` 실습


3. [**트랜잭션 이해**](https://mxxikr.github.io/posts/spring-db-transaction-understanding/)
    * 트랜잭션의 개념(ACID), DB 세션, 오토 커밋/수동 커밋의 차이 학습
    * DB 락(Lock)의 개념과 변경/조회 시의 락 획득 및 반납 과정 이해
    * 계좌 이체 비즈니스 로직을 통한 트랜잭션 적용 및 원자성 보장 테스트


4. **스프링과 문제 해결 - 트랜잭션**    - 트랜잭션 추상화(`PlatformTransactionManager`)와 트랜잭션 동기화 매니저의 역할
    * 트랜잭션 템플릿을 활용한 반복 코드 제거 및 트랜잭션 AOP(`@Transactional`) 적용
    * 스프링 부트의 자동 리소스 등록과 트랜잭션 관리의 편리함 체험


5. **자바 예외 이해**
    * 자바 예외 계층(Throwable, Error, Exception) 구조 파악
    * 체크 예외(Checked Exception)와 언체크 예외(Unchecked/Runtime Exception)의 차이 및 활용 원칙
    * 예외 전환 시 스택 트레이스(Stack Trace) 유지의 중요성 실습


6. **스프링과 문제 해결 - 예외 처리, 반복**
    * 체크 예외의 런타임 예외 변환 전략 및 인터페이스 의존 설계
    * 스프링 데이터 접근 예외 추상화(`DataAccessException`)와 `SQLExceptionTranslator` 활용
    * `JdbcTemplate` 도입을 통한 JDBC 반복 문제 해결(커넥션 동기화, 예외 변환 자동화)
