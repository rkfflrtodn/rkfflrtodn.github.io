---
layout: post
title:  "SQL-Tutorial"
date:   2018-10-04 16:01:57 +0900
categories: SQL
---

# 참고 사이트
[w3school](https://www.w3schools.com/sql/sql_intro.asp).

# SQL이란 무엇입니까?
* SQL은 구조화 된 쿼리 언어
* SQL을 사용하면 데이터베이스에 액세스하고 조작 할 수 있습니다.
* SQL은 1986 년에 미국 표준 협회 (ANSI)의 표준이되었고 1987 년에 국제 표준화기구 (ISO)의 표준이되었습니다.

# SQL은 무엇을 할 수 있습니까?
* SQL은 데이터베이스에 대해 쿼리를 실행할 수 있습니다.
* SQL은 데이터베이스에서 데이터를 검색 할 수 있습니다.
* SQL은 데이터베이스에 레코드를 삽입 할 수 있습니다.
* SQL은 데이터베이스의 레코드를 업데이트 할 수 있습니다.
* SQL은 데이터베이스에서 레코드를 삭제할 수 있습니다.
* SQL은 새로운 데이터베이스를 생성 할 수 있습니다.
* SQL은 데이터베이스에 새로운 테이블을 생성 할 수 있습니다.
* SQL은 데이터베이스에 저장 프로 시저를 생성 할 수 있습니다.
* SQL은 데이터베이스에 뷰를 생성 할 수 있습니다.
* SQL은 테이블, 프로 시저 및 뷰에 대한 사용 권한을 설정할 수 있습니다.

# 웹 사이트에서 SQL 사용
* RDBMS 데이터베이스 프로그램 (예 : MS Access, SQL Server, MySQL)
* PHP 또는 ASP와 같은 서버 측 스크립팅 언어를 사용하려면
* SQL을 사용하여 원하는 데이터를 얻으려면
* HTML / CSS를 사용하여 페이지의 스타일을 지정하려면

# RDBMS
RDBMS는 관계형 데이터베이스 관리 시스템의 약자입니다.

RDBMS는 SQL과 MS SQL Server, IBM DB2, Oracle, MySQL 및 Microsoft Access와 같은 모든 최신 데이터베이스 시스템의 기초입니다.

RDBMS의 데이터는 테이블이라는 데이터베이스 객체에 저장됩니다. 테이블은 관련 데이터 항목의 모음이며 열과 행으로 구성됩니다.

w3school에서 실습을 위해 제공하는 기본 테이블의 형태는 다음과 같다.
레코드는 총 91 개 이지만 편의상 간략히 3개만 추려서 형태만 볼 수 있게 하였다.


CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany
2 | Ana Trujillo Emparedados y helados | Ana Trujillo	 | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico
3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico


Customers이라는 Table에서 모든 자료들을 뽑아내는 데 사용하는 쿼리문은

SELECT * FROM Customers 라는 쿼리문이다.

이 쿼리문을 간단히 설명하면

'SELECT'는 뽑아낸다 라는 뜻이고

'\*'은 모든 내용을 뜻한다.

'FROM'은 FROM 뒤에 테이블 명을 입력함으로써 어느 테이블에서 앞의 쿼리문을 실행할것인지 명시한다.

위의 내용은 즉 Customers 라는 테이블에서 모든 자료를 뽑아낸다는 의미이다.


모든 테이블은 필드라는 더 작은 엔티티로 나뉩니다. Customers 테이블의 필드는 CustomerID, CustomerName, ContactName, Address, City, PostalCode 및 Country로 구성됩니다. 필드는 테이블의 모든 레코드에 대한 특정 정보를 유지 관리하도록 설계된 테이블의 열입니다.

레코드라고도하는 레코드는 테이블에있는 개별 항목입니다. 예를 들어, 위의 Customers 테이블에는 91 개의 레코드가 있습니다. 레코드는 테이블의 가로 엔티티입니다.

컬럼은 테이블의 특정 필드와 연관된 모든 정보를 포함하는 테이블의 수직 엔티티입니다.

**참고로 SQL 키워드는 대소 문자를 구분하지 않습니다. select는 SELECT와 같습니다.**


# SQL 문 다음에 오는 세미콜론?
일부 데이터베이스 시스템에서는 각 SQL 문의 끝에 세미콜론이 필요합니다.

세미콜론은 데이터베이스 시스템에서 각 SQL 문을 분리하여 서버에 대한 동일한 호출에서 둘 이상의 SQL 문을 실행할 수 있도록하는 표준 방법입니다.

이 튜토리얼에서는 각 SQL 문의 끝에 세미콜론을 사용합니다.

# 가장 자주 사용되는 SQL명령들..

* **SELECT** - 데이터베이스에서 데이터를 추출합니다.
* **UPDATE** - 데이터베이스의 데이터를 업데이트합니다.
* **DELETE** - 데이터베이스에서 데이터를 삭제합니다.
* **INSERT INTO** - 새로운 데이터를 데이터베이스에 삽입합니다.
* **CREATE DATABASE** - 새 데이터베이스를 만듭니다.
* **ALTER DATABASE** - 데이터베이스를 수정합니다.
* **CREATE TABLE** - 새 테이블을 만듭니다.
* **ALTER TABLE** - 테이블을 수정합니다.
* **DROP TABLE** - 테이블을 삭제합니다.
* **CREATE INDEX** - 색인 (검색 키)을 작성합니다.
* **DROP INDEX** - 색인을 삭제합니다.


# SQL SELECT 문

## SQL SELECT 문
~~~SQL
SELECT 문은 데이터베이스에서 데이터를 선택하는 데 사용됩니다.

리턴 된 데이터는 결과 세트라고하는 결과 테이블에 저장됩니다.
~~~
## SELECT 구문
~~~SQL
SELECT column1, column2, ...  
FROM table_name;
~~~
## 예
~~~SQL
SELECT CustomerName, City FROM Customers;
~~~

# SQL SELECT DISTINCT 문

## SQL SELECT DISTINCT 문

SELECT DISTINCT.은 고유 한 (다른) 값만 리턴하는 데 사용됩니다.

테이블 내에서 열은 종종 많은 중복 값을 포함합니다. 때로는 서로 다른 (뚜렷한) 값만 나열하려고합니다.

SELECT DISTINCT.은 고유 한 (다른) 값만 리턴하는 데 사용됩니다.

## SELECT DISTINCT 구문
~~~SQL
SELECT DISTINCT column1, column2, ...  
FROM table_name;
~~~
## 예
~~~SQL
SELECT DISTINCT Country FROM Customers;
~~~

# SQL WHERE 절

## SQL WHERE 절

WHERE 절은 레코드를 필터링하는 데 사용됩니다.

WHERE 절은 지정된 조건을 충족하는 레코드 만 추출하는 데 사용됩니다.

## WHERE 구문
~~~SQL
SELECT column1, column2, ...  
FROM table_name  
WHERE condition;
~~~
## 예
~~~SQL
SELECT * FROM Customers  
WHERE Country='Mexico';
~~~
## 텍스트 필드와 숫자 필드 비교

SQL은 텍스트 값에 대해 작은 따옴표를 사용해야합니다 (대부분의 데이터베이스 시스템은 큰 따옴표도 허용합니다).

그러나 숫자 필드는 따옴표로 묶지 않아야합니다.

## 예
~~~SQL
SELECT * FROM Customers  
WHERE CustomerID=1;
~~~
