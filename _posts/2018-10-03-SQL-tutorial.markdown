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
---

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



## SQL SELECT 문
~~~SQL
SELECT 문은 데이터베이스에서 데이터를 선택하는 데 사용됩니다.

리턴 된 데이터는 결과 세트라고하는 결과 테이블에 저장됩니다.
~~~
# SELECT 구문
~~~SQL
SELECT column1, column2, ...  
FROM table_name;
~~~
# 예
~~~SQL
SELECT CustomerName, City FROM Customers;
~~~


## SQL SELECT DISTINCT 문

SELECT DISTINCT.은 고유 한 (다른) 값만 리턴하는 데 사용됩니다.

테이블 내에서 열은 종종 많은 중복 값을 포함합니다. 때로는 서로 다른 (뚜렷한) 값만 나열하려고합니다.

SELECT DISTINCT.은 고유 한 (다른) 값만 리턴하는 데 사용됩니다.

# SELECT DISTINCT 구문
~~~SQL
SELECT DISTINCT column1, column2, ...  
FROM table_name;
~~~
# 예
~~~SQL
SELECT DISTINCT Country FROM Customers;
~~~


## SQL WHERE 절

WHERE 절은 레코드를 필터링하는 데 사용됩니다.

WHERE 절은 지정된 조건을 충족하는 레코드 만 추출하는 데 사용됩니다.

# WHERE 구문
~~~SQL
SELECT column1, column2, ...  
FROM table_name  
WHERE condition;
~~~
# 예
~~~SQL
SELECT * FROM Customers  
WHERE Country='Mexico';
~~~
# 텍스트 필드와 숫자 필드 비교

SQL은 텍스트 값에 대해 작은 따옴표를 사용해야합니다 (대부분의 데이터베이스 시스템은 큰 따옴표도 허용합니다).

그러나 숫자 필드는 따옴표로 묶지 않아야합니다.

# 예
~~~SQL
SELECT * FROM Customers  
WHERE CustomerID=1;
~~~

# WHERE 절에있는 연산자

다음 연산자는 WHERE 절에서 사용할 수 있습니다.

Operator | Description
---------| ------------------------------------
= |	Equal
<> |	Not equal. Note: In some versions of SQL this operator may be written as !=
\> |	Greater than
< |	Less than
\>= |	Greater than or equal
<= |	Less than or equal
BETWEEN |	Between a certain range
LIKE |	Search for a pattern
IN |	To specify multiple possible values for a column


## SQL AND, OR 및 NOT 연산자

WHERE 절은 AND, OR 및 NOT 연산자와 결합 할 수 있습니다.

AND 및 OR 연산자는 둘 이상의 조건에 따라 레코드를 필터링하는 데 사용됩니다.

* AND로 구분 된 모든 조건이 TRUE이면 AND 연산자는 레코드를 표시합니다.  
* OR로 구분 된 조건이 TRUE 인 경우 OR 연산자는 레코드를 표시합니다.

NOT 연산자는 조건이 참이 아닌 경우 레코드를 표시합니다.


# AND 구문

~~~SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
~~~

# OR 구문

~~~SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
~~~

# NOT 문법

~~~SQL
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
~~~

## SQL ORDER BY 키워드

ORDER BY 키워드는 결과 집합을 오름차순 또는 내림차순으로 정렬하는 데 사용됩니다.

ORDER BY 키워드는 기본적으로 레코드를 오름차순으로 정렬합니다. 내림차순으로 레코드를 정렬하려면 DESC 키워드를 사용하십시오.

# ORDER BY 구문

~~~SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
~~~


## SQL INSERT INTO 문

INSERT INTO 문은 테이블에 새 레코드를 삽입하는 데 사용됩니다.

# INSERT INTO 구문

두 가지 방법으로 INSERT INTO 문을 작성할 수 있습니다.

첫 번째 방법은 삽입 할 열 이름과 값을 모두 지정합니다.

~~~SQL
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
~~~

표의 모든 열에 값을 추가하는 경우 SQL 조회에서 열 이름을 지정할 필요가 없습니다.  
그러나 값의 순서가 표의 열과 동일한 순서인지 확인하십시오.  
INSERT INTO 구문은 다음과 같습니다.

~~~SQL
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
~~~


## SQL NULL 값

# NULL 값이란 무엇입니까?

NULL 값이있는 필드는 값이없는 필드입니다.

테이블의 필드가 선택적이면이 필드에 값을 추가하지 않고 새 레코드를 삽입하거나 레코드를 업데이트 할 수 있습니다. 그런 다음 필드는 NULL 값으로 저장됩니다.

**참고** : NULL 값이 0 값 또는 공백이있는 필드와 다른 것을 이해하는 것이 매우 중요합니다. NULL 값이있는 필드는 레코드를 생성하는 동안 비어있는 필드입니다.

# NULL 값을 테스트하는 방법?

=, <또는 <>과 같은 비교 연산자로 NULL 값을 테스트 할 수 없습니다.

대신에 IS NULL 연산자와 IS NOT NULL 연산자를 사용해야합니다.

# IS NULL 구문

~~~SQL
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
~~~

# IS NOT NULL 구문

~~~SQL
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
~~~

# IS NULL 연산자

다음 SQL.은 IS NULL 연산자를 사용하여 주소가없는 모든 g 원을 나열합니다.

~~~SQL
SELECT LastName, FirstName, Address FROM Persons
WHERE Address IS NULL;
~~~

결과 세트는 다음과 같습니다.

LastName |	FirstName |	Address
---------|------------| -------
Bloggs |	Joe	 
Roe |	Jane

# IS NOT NULL 연산자

다음 SQL 문은 IS NOT NULL 연산자를 사용하여 주소가있는 모든 사람을 나열합니다.

~~~SQL
SELECT LastName, FirstName, Address FROM Persons
WHERE Address IS NOT NULL;
~~~

결과 세트는 다음과 같습니다.

LastName |	FirstName |	Address
---------| ---------- | --------
Doe |	John | 542 W. 27th Street
Smith |	John | 110 Bishopsgate


## SQL UPDATE 문


UPDATE 문은 테이블의 기존 레코드를 수정하는 데 사용됩니다.

# UPDATE 구문

~~~SQL
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
~~~

**참고** : 테이블에서 레코드를 업데이트 할 때주의하십시오! UPDATE 문에서 WHERE 절을 확인하십시오. WHERE 절은 갱신해야하는 레코드를 지정합니다. WHERE 절을 생략하면 테이블의 모든 레코드가 업데이트됩니다!

# 테이블 업데이트

다음 SQL 문은 첫 번째 고객 (CustomerID = 1)을 새 담당자 및 새 도시로 업데이트합니다.

~~~SQL
UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;
~~~

# 여러 레코드 업데이트

업데이트 될 레코드 수를 결정하는 것은 WHERE 절입니다.

다음 SQL 문은 country가 "Mexico"인 모든 레코드에 대해 연락처 이름을 "Juan"으로 업데이트합니다.

~~~SQL
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';
~~~

# UPDATE 사용시 주의 할점
레코드를 업데이트 할 때는주의하십시오. **WHERE 절을 생략하면 모든 레코드가 업데이트됩니다!**


## SQL DELETE 문

DELETE 문은 테이블의 기존 레코드를 삭제하는 데 사용됩니다.

# DELETE 구문
~~~SQL
DELETE FROM table_name
WHERE condition;
~~~

# DELETE 사용시 주의 할점
테이블에서 레코드를 삭제할 때주의하십시오! DELETE 문의 WHERE 절을 확인하십시오. WHERE 절은 h 제될 레코드를 지정합니다. **WHERE 절을 생략하면 테이블의 모든 레코드가 삭제됩니다!**


## SQL SELECT TOP 절

SELECT TOP 절은 리턴 할 레코드 수를 지정하는 데 사용됩니다.

SELECT TOP 절은 수천 개의 레코드가있는 큰 테이블에서 유용합니다. 많은 수의 레코드를 반환하면 성능에 영향을 줄 수 있습니다.

노트 : 모든 데이터베이스 시스템이 SELECT TOP 절을 지원하는 것은 아닙니다. MySQL은 제한된 수의 레코드를 선택하기 위해 LIMIT 절을 지원하고 Oracle은 ROWNUM을 사용합니다.

**SQL Server / MS 액세스 구문 :**

~~~SQL
SELECT TOP number|percent column_name(s)
FROM table_name
WHERE condition;
~~~

**MySQL 구문 :**
~~~SQL
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
~~~

**Oracle 구문 :**
~~~SQL
SELECT column_name(s)
FROM table_name
WHERE ROWNUM <= number;
~~~


## SQL MIN () 및 MAX () 함수

MIN () 함수는 선택된 컬럼의 가장 작은 값을 리턴합니다.

MAX () 함수는 선택된 열의 가장 큰 값을 반환합니다.

# MIN () 구문
~~~SQL
SELECT MIN(column_name)
FROM table_name
WHERE condition;
~~~

# MAX () 구문
~~~SQL
SELECT MAX(column_name)
FROM table_name
WHERE condition;
~~~

## SQL COUNT (), AVG () 및 SUM () 함수

COUNT () 함수는 지정된 기준과 일치하는 행 수를 반환합니다.

AVG () 함수는 숫자 열의 평균값을 반환합니다.

SUM () 함수는 숫자 열의 총 합계를 반환합니다.

# COUNT () 구문
~~~SQL
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
~~~
# AVG () 구문
~~~SQL
SELECT AVG(column_name)
FROM table_name
WHERE condition;
~~~
# SUM () 구문
~~~SQL
SELECT SUM(column_name)
FROM table_name
WHERE condition;
~~~

## SQL LIKE 연산자

LIKE 연산자는 WHERE 절에서 열의 지정된 패턴을 검색하는 데 사용됩니다.

LIKE 연산자와 함께 사용되는 두 개의 와일드 카드가 있습니다.

* % - 백분율 기호는 0, 1 또는 복수 문자를 나타냅니다.
* _ - 밑줄은 한 문자를 나타냅니다.

**참고** : MS Access는 밑줄 (\_) 대신 물음표 (?)를 사용합니다.

백분율 기호와 밑줄은 조합하여 사용할 수도 있습니다!

# LIKE 구문
~~~SQL
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
~~~

**팁** : AND 또는 OR 연산자를 사용하여 여러 조건을 결합 할 수도 있습니다.

다음은 '%'와 '\_'와일드 카드가있는 다른 LIKE 연산자를 보여주는 몇 가지 예입니다.

LIKE Operator |	Description
--------------------------- | ---------------------------------
WHERE CustomerName LIKE 'a%'|	Finds any values that start with "a"
WHERE CustomerName LIKE '%a'|	Finds any values that end with "a"
WHERE CustomerName LIKE '%or%'|	Finds any values that have "or" in any position
WHERE CustomerName LIKE '\_r%' |	Finds any values that have "r" in the second position
WHERE CustomerName LIKE 'a_%\_%' |	Finds any values that start with "a" and are at least 3 characters in length
WHERE ContactName LIKE 'a%o'|	Finds any values that start with "a" and ends with "o"


## SQL 와일드 카드 문자

와일드 카드 문자는 문자열의 다른 문자를 대체하는 데 사용됩니다.

와일드 카드 문자는 SQL LIKE 연산자 와 함께 사용됩니다 . LIKE 연산자는 WHERE 절에서 열의 지정된 패턴을 검색하는 데 사용됩니다.

LIKE 연산자와 함께 사용되는 두 개의 와일드 카드가 있습니다.

* % - 백분율 기호는 0, 1 또는 복수 문자를 나타냅니다.
* _ - 밑줄은 한 문자를 나타냅니다.

**참고** : MS Access는 밑줄 (\_) 대신 물음표 (?)를 사용합니다.

MS Access 및 SQL Server에서는 다음을 사용할 수도 있습니다.

* [ charlist ] - 일치시킬 문자와 세트의 범위를 정의합니다.
* [^ charlist ] 또는 [! charlist ] - 일치하지 않는 문자의 집합과 범위를 정의합니다.
와일드 카드는 조합하여 사용할 수도 있습니다!

다음은 '%'와 '\_'와일드 카드가있는 다른 LIKE 연산자를 보여주는 몇 가지 예입니다.

LIKE Operator	| Description
--------------|----------------
WHERE CustomerName LIKE 'a%'|	Finds any values that starts with "a"
WHERE CustomerName LIKE '%a'|	Finds any values that ends with "a"
WHERE CustomerName LIKE '%or%'|	Finds any values that have "or" in any position
WHERE CustomerName LIKE '\_r%'|	Finds any values that have "r" in the second position
WHERE CustomerName LIKE 'a_%\_%'|	Finds any values that starts with "a" and are at least 3 characters in length
WHERE ContactName LIKE 'a%o'|	Finds any values that starts with "a" and ends with "o"


## SQL IN 연산자

IN 연산자를 사용하여 WHERE 절에 여러 값을 지정할 수 있습니다.

IN 연산자는 여러 OR 조건의 줄임말입니다.

# IN 구문
~~~SQL
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
~~~

또는:

~~~SQL
SELECT column_name(s)
FROM table_name
WHERE column_name IN (SELECT STATEMENT);
~~~

## SQL BETWEEN 연산자

BETWEEN 연산자는 주어진 범위 내의 값을 선택합니다. 값은 숫자, 텍스트 또는 날짜 일 수 있습니다.

BETWEEN 연산자는 시작과 끝 값이 포함됩니다.

# BETWEEN 구문
~~~SQL
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
~~~

## SQL Aliases(별명)

SQL aliases는 테이블 또는 테이블의 열에 임시 이름을 지정하는 데 사용됩니다.

Aliases는 컬럼 이름을 읽기 쉽게하기 위해 자주 사용됩니다.

alias은 조회 기간 동안 만 존재합니다.

# alias 열 구문
~~~SQL
SELECT column_name AS alias_name
FROM table_name;
~~~
# alias 테이블 구문
~~~SQL
SELECT column_name(s)
FROM table_name AS alias_name;
~~~


## SQL JOIN
JOIN 절은 두 개 이상의 테이블에있는 행을 결합하는 데 사용됩니다.

'주문'표에서 선택 항목을 살펴 보겠습니다.

OrderID |	CustomerID|	OrderDate
--------|-----------|----------
10308	|2|	1996-09-18
10309	|37|	1996-09-19
10310	|77|	1996-09-20

그런 다음 '고객'표에서 선택 항목을 살펴보십시오.

CustomerID|	CustomerName	|ContactName	Country
----------|---------------|--------------------
1|	Alfreds Futterkiste|	Maria Anders	Germany
2|	Ana Trujillo Emparedados y helados|	Ana Trujillo	Mexico
3|	Antonio Moreno Taquería|	Antonio Moreno	Mexico

"주문"테이블의 "고객 ID"열은 "고객"테이블의 "고객 ID"를 나타냅니다. 위의 두 테이블 사이의 관계는 "CustomerID"열입니다.

그런 다음 두 테이블에서 일치하는 값을 가진 레코드를 선택하는 다음 SQL 문 (INNER JOIN 포함)을 작성할 수 있습니다.

# 예
~~~SQL
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders
INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
~~~

그러면 다음과 같은 결과가 나옵니다.

OrderID	|CustomerName|	OrderDate
--------|------------|-----------
10308	|Ana Trujillo Emparedados y helados	|9/18/1996
10365	|Antonio Moreno Taquería	|11/27/1996
10383	|Around the Horn	|12/16/1996
10355	|Around the Horn	|11/15/1996
10278	|Berglunds snabbköp	|8/12/1996

# 다양한 유형의 SQL JOIN
다음은 SQL에있는 JOIN의 여러 유형입니다.

* (INNER) JOIN : 두 테이블에서 값이 일치하는 레코드를 반환합니다.
* LEFT (OUTER) JOIN : 왼쪽 테이블에서 모든 레코드를 반환하고 오른쪽 테이블에서 일치하는 레코드를 반환합니다.
* RIGHT (OUTER) JOIN : 오른쪽 테이블에서 모든 레코드를 반환하고 왼쪽 테이블에서 일치하는 레코드를 반환합니다.
* FULL (OUTER) JOIN : 왼쪽 또는 오른쪽 테이블에 일치하는 항목이 있으면 모든 레코드를 반환합니다.

![innerjoin](../img/ij.gif)
![leftjoin](../img/lj.gif)
![rightjoin](../img/rj.gif)
![fullouterjoin](../img/foj.gif)
