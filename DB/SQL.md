# 완료

## 📌 SQL(Structured Query Langauge)이란?

- 관계형 데이터베이스 관리 시스템(RDBMS)의 데이터를 관리 및 처리하기 위해 설계된 특수 목적의 프로그래밍 언어이다.
- SQL문 실행순서 vs 작성순서
    
    ⑤ SELECT
    
    ① FROM
    
    ② WHERE
    
    ③ GROUP BY
    
    ④ HAVING
    
    ⑥ ORDER BY
    

---

## 📌 RDBMS vs DBMS

### DBMS(DataBase Management System)

- DBMS는 데이터베이스를 관리하는 시스템이다.
- 사용자와 DB사이에서 사용자의 요구에 따라 데이터를 생성해주고, DB를 관리해주는 소프트웨어이다.
- DBMS는 데이터를 계층 또는 탐색 형식으로 저장한다. 파일 시스템을 사용해 저장하며, 따라서 테이블 간에는 아무런 관계가 없다.
- 데이터에 대한 많은 보안을 제공하지 않으며 정규화를 수행할 수 없어 데이터는 높은 중복성을 가질 수 있다.
- Sybase, dbase 및 Microsoft Access는 DBMS의 몇 가지 예이다.

### RDBMS(Relational DataBase Management System)

- RDB를 생성하고 수정하고 관리할 수 있는 소프트웨어이다.
- RDBMS는 관계형 모델을 기반으로 하는 DBMS 유형이다.
- RDBMS의 테이블은 서로 연관되어 있어 일반 DBMS보다 효율적으로 데이터를 저장, 구성 및 관리할 수 있다.
- 정규화를 통해 데이터의 중복성을 최소화하여 트랜잭션을 수행하는 것이 더 쉽다.
- 데이터의 원자성, 일관성, 격리 및 내구성을 유지하며 데이터 무결성을 높인다.
- MSSQL, MySQL, Oracle이 RDBMS의 몇 가지 예이다.

무결성

RDBMS 

**⭐️ 즉, RDBMS는 DBMS의 한 종류이다.**

---

## 📌 SQL의 종류

![스크린샷 2023-05-29 오전 1.51.56.png](%E1%84%8B%E1%85%AA%E1%86%AB%E1%84%85%E1%85%AD%200640d91cd88c4e4383da9b07ee281389/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-05-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_1.51.56.png)

SQL은 크게 세 가지로 종류로 나뉜다.

- DDL(Data Definition Language) : 데이터 정의 언어
- DML(Data Manipulation Language) : 데이터 처리 언어
- DCL(Data Control Language) : 데이터 제어 언어

### DDL(**Data Definition Language)**

데이터를 정의할 때 사용하는 언어이다.

| 명령어 | 내용 |
| --- | --- |
| CREATE | 테이블을 생성하는 역할 |
| ALTER | 테이블의 구조를 수정하는 역할 |
| DROP | 테이블을 삭제하는 역할 |
| RENAME | 테이블을 이름을 변경하는 역할 |
| TRUNCATE | 테이블을 초기화하는 역할 |

### DML**(Data Manipulation Language)**

데이터베이스에 데이터를 저장할 때 사용하는 언어이다.

| 명령어 | 내용 |
| --- | --- |
| SELECT | 데이터베이스에서 데이터를 검색하는 역할 |
| INSERT | 테이블에 데이터를 추가하는 역할 |
| UPDATE | 테이블 내에 존재하는 데이터를 수정하는 역할 |
| DELETE | 테이블에서 데이터를 삭제하는 역할 |
| TRUNCATE | 테이블을 초기화하는 역할 |

### **DCL (Data Control Language)**

DCL(Data Control Language)은 데이터베이스에 대한 접근 권한과 관련된 문법으로, 어느 유저가 데이터베이스에 접근할 수 있는지 권한을 설정한다. 

| 명령어 | 내용 |
| --- | --- |
| GRANT | 권한을 정의할때 사용하는 명령어 |
| REVOKE | 권한을 삭제할때 사용하는 명령어 |

### T**CL (Transaction Control Language)**

DCL과 비슷한 맥락이지만 데이터를 제어하는 언어가 아닌 **`트랜잭션`**을 제어할때 사용한다. 논리적인 작업 단위를 묶어 DML에 의해 조작된 결과를 **`트랜잭션`** 별로 제어한다.

| 명령어 | 내용 |
| --- | --- |
| COMMIT | 모든 작업을 정상적으로 처리하겠다는 명령어 |
| ROLLBACK | 모든 작업을 다시 돌려 놓겠다는 명령어 |
| SAVEPOINT | Commit 전에 특정 시점까지만 반영하거나 Rollback하겠다는 명령어 |

<aside>
💡 **트랜잭션이란?** 
하나의 작업을 위해 더이상 분할될 수 없는 명령들의 모음, 즉, 한꺼번에 **수행되어야 할 일련의 연산모음**을 의미한다.
[예시](https://inpa.tistory.com/entry/MYSQL-%F0%9F%93%9A-%ED%8A%B8%EB%9E%9C%EC%9E%AD%EC%85%98Transaction-%EC%9D%B4%EB%9E%80-%F0%9F%92%AF-%EC%A0%95%EB%A6%AC#%ED%8A%B8%EB%9E%9C%EC%9E%AD%EC%85%98transaction_%EC%9D%B4%EB%9E%80?)
**트랜잭션의 특징**

| 이름 | 내용 |
| --- | --- |
| 원자성 (Atomicity) | 원자성은 트랜잭션이 데이터베이스에 모두 반영되던가, 아니면 전혀 반영되지 않아야 한다는 것이다. |
| 일관성 (Consistency) | 일관성은 트랜잭션의 작업 처리 결과가 항상 일관성이 있어야 한다는 것이다. 
예시) 데이터타입이 정수형에서 갑자기 문자열로 바뀌면 안됨. |
| 독립성 (Isolation) | 둘 이상의 트랜잭션이 동시에 실행되고 있을 경우
어떤 하나의 트랜잭션이라도, 다른 트랜잭션의 연산에 끼어들 수 없다는 점을 가리킨다. |
| 영구성 (Durability) | 지속성은 트랜잭션이 성공적으로 완료됬을 경우, 결과는 영구적으로 반영되어야 한다는 점이다. |
|  |  |
</aside>

### 번외

**DQL(Data Query Language)**

DQL(Data Query Language)은 정해진 스키마 내에서 쿼리할 수 있는 언어로, 대표적으로`SELECT` 가 DQL에 해당하며 DQL을 DML의 일부분으로 취급하기도 한다.

- SELECT: 테이블 내의 데이터를 조회할 때 사용
- WHERE: 테이블에 저장된 데이터 중 원하는 데이터만 선택적으로 추출한다.
- DISTINCT: 동일한 값의 중복을 제거한다.
- GROUP BY: 해당 값을 그룹화하여 출력한다.
- ORDER BY: 특정 칼럼을 기준으로 순서대로 나열한다(ASC - 오름차순(기본값), DESC - 내림차순)

---

## 📌 DISTINCT vs GROUP BY

**DISTINCT**

DISTINCT 키워드를 사용하여 데이터 중복을 제거할 때는 DISTINCT 키워드만 명시하면 되므로 쿼리문이 간결하다. 하지만 TEMP TABLESPCE를 생성하여 임시로 저장하고 작업하는 방식이라 시스템 부하가 크다.

**GROUP BY**

GROUP BY 절을 이용하면 간결하게 명시할 수 있으며 DISTINCT와 다르게 시스템 부하가 적다.

[추가정보](http://intomysql.blogspot.com/2011/01/distinct-group-by.html)

---

## 📌 **TRUNCATE와 DELETE**

**TRUNCATE TABLE**

시스템 부하가 적다. DELETE와 다르게 데이터 전체를 날려버리기 때문에 메모리를 많이 차지 하지 않는다. 하지만 이때문에 정상적인 데이터 복구가 불가능하다. 

**DELETE**

시스템 부하가 크다. 데이터 전체를 삭제 하는것이 아니라 복구할 수 있게끔 삭세하기 때문에 메모리를 많이 차지한다. 하지만 반대로 정상적인 복구가 가능성이 높다.

---

## 📌 **트랜잭션의 Commit과 Rollback**

**Commit**

Commit은 모든 작업들을 정상 처리하겠다고 확정하는 명령어이다. 해당 처리 과정을 DB에 영구 저장하겠다는 의미로 Commit을 수행하면 하나의 트랜잭션 과정이 종료된다. Commit을 하기 전에는 다른 사용자가 트랜잭션 내용을 확인할 수 없다. 또한, 변경된 행은 잠금이 설정되어 있어서 다른 사용자가 변경할 수 없다.

**Rollback**

Roll-back은 작업 중 문제가 발생되어 트랜잭션의 처리 과정에서 발생한 변경사항을 취소하는 명령어이다. 해당 명령을 트랜잭션에게 하달하면 트랜잭션은 Commit 되기 이전의 데이터오 돌아가 변경에 대하여 취소한다. 관련된 행에 대한 잠금이 풀리고 데이터 변경 사항이 복구되는 것이다.

unique key 중복값 허용 x