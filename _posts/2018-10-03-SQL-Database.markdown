---
layout: post
title:  "SQL-Database"
date:   2018-10-04 16:01:57 +0900
categories: SQL
---

## SQL CREATE DATABASE 문
CREATE DATABASE 문은 새 SQL 데이터베이스를 만드는 데 사용됩니다.

# 문법
~~~SQL
CREATE DATABASE databasename;
~~~

## SQL DROP DATABASE 문
DROP DATABASE 문은 기존 SQL 데이터베이스를 삭제하는 데 사용됩니다.

# 문법
~~~SQL
DROP DATABASE databasename;
~~~

*노트* : 데이터베이스를 h 제하기 전에주의하십시오. 데이터베이스를 삭제하면 데이터베이스에 저장된 완전한 정보가 손실됩니다!


## SQL CREATE TABLE 문
CREATE TABLE 문은 데이터베이스에 새 테이블을 만드는 데 사용됩니다.

# 문법
~~~SQL
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
~~~
column 매개 변수는 테이블의 열 이름을 지정합니다.

datatype 매개 변수는 열에서 보유 할 수있는 데이터 유형 (예 : varchar, 정수, 날짜 등)을 지정합니다.

**팁** : 사용 가능한 데이터 유형에 대한 개요는 전체 데이터 유형 참조로 이동하십시오 .


# SQL DROP TABLE 문
DROP TABLE 문은 데이터베이스의 기존 테이블을 삭제하는 데 사용됩니다.

# 문법
~~~SQL
DROP TABLE table_name;
~~~
**참고** : 테이블을 떨어 뜨리기 전에주의하십시오. 테이블을 삭제하면 테이블에 저장된 완전한 정보가 손실됩니다!


## SQL ALTER TABLE 문
ALTER TABLE 문은 기존 테이블의 열을 추가, 삭제 또는 수정하는 데 사용됩니다.

ALTER TABLE.은 기존 테이블에 다양한 제한 조건을 추가 W h 제하는 데에도 사용됩니다.

# ALTER TABLE - 열 추가
테이블에 열을 추가하려면 다음 구문을 사용하십시오.

~~~SQL
ALTER TABLE table_name
ADD column_name datatype;
~~~

# ALTER TABLE - 열 삭제
테이블의 열을 삭제하려면 다음 구문을 사용하십시오 (일부 데이터베이스 시스템에서는 열 삭제가 허용되지 않음).
~~~SQL
ALTER TABLE table_name
DROP COLUMN column_name;
~~~

# ALTER TABLE - ALTER / MODIFY COLUMN
테이블에있는 열의 데이터 형식을 변경하려면 다음 구문을 사용합니다.

**SQL Server / MS 액세스 :**
~~~SQL
ALTER TABLE table_name
ALTER COLUMN column_name datatype;
~~~

**MySQL / Oracle (이전 버전 10G) :**
~~~SQL
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
~~~

**Oracle 10G 이상 :**
~~~SQL
ALTER TABLE table_name
MODIFY column_name datatype;
~~~


## SQL Constraints(제약)

SQL 제한 조건은 테이블의 데이터에 대한 j을 지정하는 데 사용됩니다.

SQL 제약 조건 만들기
CREATE TABLE.으로 테이블이 작성 될 때 또는 ALTER TABLE.으로 테이블이 작성된 후에 제한 조건을 지정할 수 있습니다.

# 문법
~~~SQL
CREATE TABLE table_name (
    column1 datatype constraint,
    column2 datatype constraint,
    column3 datatype constraint,
    ....
);
~~~

# SQL 제약
SQL 제약 조건은 테이블의 데이터에 대한 규칙을 지정하는 데 사용됩니다.

제약 조건은 테이블에 들어갈 수있는 데이터 유형을 제한하는 데 사용됩니다. 이렇게하면 표의 데이터 정확성과 신뢰성이 보장됩니다. 제한 조건과 데이터 조치 사이에 위반이 있으면 조치가 중단됩니다.

제약 조건은 열 수준 또는 테이블 수준 일 수 있습니다. 컬럼 레벨 제한 조건은 컬럼에 적용되고 테이블 레벨 제한 조건은 전체 테이블에 적용됩니다.

SQL에서 일반적으로 사용되는 다음 제약 조건이 있습니다.

* **NOT NULL** - 열이 NULL 값을 가질 수 없음을 보장합니다.
* **UNIQUE** - 열의 모든 값이 서로 다른지 확인합니다.
* **PRIMARY KEY** - NOT NULL과 UNIQUE의 조합. 테이블의 각 행을 고유하게 식별합니다.
* **FOREIGN KEY** - 다른 테이블의 행 / 레코드를 고유하게 식별합니다.
* **CHECK** - 열의 모든 값이 특정 조건을 충족하는지 확인합니다.
* **DEFAULT** - 값이 지정되지 않은 경우 열의 기본값을 설정합니다.
* **INDEX** - 데이터베이스에서 데이터를 매우 신속하게 생성 및 검색하는 데 사용됩니다.

## SQL NOT NULL 제약 조건

기본적으로 열은 NULL 값을 포함 할 수 있습니다.

NOT NULL 제약 조건은 열이 NULL 값을 허용하지 않도록 강제합니다.

이렇게하면 필드에 항상 값이 포함될 수 있습니다. 즉, 새 레코드를 삽입하거나이 필드에 값을 추가하지 않고 레코드를 업데이트 할 수 없습니다.

다음 SQL은 "ID", "LastName"및 "FirstName"열이 NULL 값을 허용하지 않도록합니다.

# 예
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255) NOT NULL,
    Age int
);
~~~


## SQL UNIQUE 제약 조건
UNIQUE 제약 조건은 열의 모든 값이 서로 다른지 확인합니다.

UNIQUE 및 PRIMARY KEY 제약 조건은 열 또는 열 집합의 고유성을 보장합니다.

PRIMARY KEY 제약 조건에는 자동으로 UNIQUE 제약 조건이 있습니다.

그러나 테이블 당 많은 UNIQUE 제약 조건을 가질 수 있지만 테이블 당 하나의 PRIMARY KEY 제약 조건 만 가질 수 있습니다.

# CREATE TABLE에 대한 SQL UNIQUE 제약 조건
다음 SQL은 "Person"테이블을 만들 때 "ID"열에 UNIQUE 제약 조건을 만듭니다.

**SQL Server / Oracle / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL UNIQUE,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
~~~
**MySQL :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    UNIQUE (ID)
);
~~~

UNIQUE 제약 조건의 이름을 지정하고 여러 열에 UNIQUE 제약 조건을 정의하려면 다음 SQL 구문을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT UC_Person UNIQUE (ID,LastName)
);
~~~

## ALTER TABLE에 대한 SQL UNIQUE 제약

테이블이 이미 만들어 졌을 때 "ID"열에 UNIQUE 제약 조건을 만들려면 다음 SQL을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD UNIQUE (ID);
~~~
UNIQUE 제약 조건의 이름을 지정하고 여러 열에 UNIQUE 제약 조건을 정의하려면 다음 SQL 구문을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD CONSTRAINT UC_Person UNIQUE (ID,LastName);
UNIQUE 제약 조건 삭제
UNIQUE 제약 조건을 삭제하려면 다음 SQL을 사용하십시오.
~~~
**MySQL :**
~~~SQL
ALTER TABLE Persons
DROP INDEX UC_Person;
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
DROP CONSTRAINT UC_Person;
~~~


## SQL PRIMARY KEY 제약

PRIMARY KEY 제약 조건은 데이터베이스 테이블의 각 레코드를 고유하게 식별합니다.

기본 키는 UNIQUE 값을 포함해야하며 NULL 값을 포함 할 수 없습니다.

테이블에는 기본 키가 하나만있을 수 있습니다. 기본 키는 하나 또는 여러 개의 필드로 구성 될 수 있습니다.

# CREATE TABLE의 SQL PRIMARY KEY
다음 SQL은 "Person"테이블이 생성 될 때 "ID"열에 PRIMARY KEY를 만듭니다.

**MySQL :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL PRIMARY KEY,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
~~~
PRIMARY KEY 제약 조건의 이름 지정을 허용하고 여러 열에 대해 PRIMARY KEY 제약 조건을 정의하려면 다음 SQL 구문을 사용합니다.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CONSTRAINT PK_Person PRIMARY KEY (ID,LastName)
);
~~~

**참고** : 위의 예에서는 오직 하나의 PRIMARY KEY (PK_Person) 만 있습니다. 그러나 기본 키의 VALUE는 두 개의 COLUMNS (ID + 성)로 구성됩니다.


## ALTER TABLE에 대한 SQL PRIMARY KEY
테이블이 이미 만들어 졌을 때 "ID"열에 PRIMARY KEY 제약 조건을 만들려면 다음 SQL을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD PRIMARY KEY (ID);
~~~
PRIMARY KEY 제약 조건의 이름 지정을 허용하고 여러 열에 대해 PRIMARY KEY 제약 조건을 정의하려면 다음 SQL 구문을 사용합니다.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastName);
~~~
**노트** : ALTER TABLE 문을 사용하여 기본 키를 추가하는 경우 기본 키 열은 (테이블이 처음 작성되었을 때) NULL 값을 포함하지 않도록 이미 선언되어 있어야합니다.

# PRIMARY KEY 제약 조건 삭제
PRIMARY KEY 제약 조건을 삭제하려면 다음 SQL을 사용하십시오.

**MySQL :**
~~~SQL
ALTER TABLE Persons
DROP PRIMARY KEY;
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
DROP CONSTRAINT PK_Person;
~~~


## SQL FOREIGN KEY 제약
외래 키는 두 테이블을 서로 연결하는 데 사용되는 키입니다.

외부 키는 다른 테이블의 PRIMARY KEY를 참조하는 테이블의 필드 (또는 필드 모음)입니다.

외래 키가 들어있는 테이블을 하위 테이블이라고하고 후보 키가 들어있는 테이블을 참조 된 테이블 또는 상위 테이블이라고합니다.

다음 두 테이블을보십시오.

"**Persons**" table:

PersonID|	LastName|	FirstName	Age
--------|---------|------------
1|	Hansen	|Ola|	30
2|	Svendson|	Tove|	23
3|	Pettersen|	Kari|	20

"**Orders**" table:

OrderID	|OrderNumber|	PersonID
--------|-----------|---------
1|	77895|	3
2|	44678|	3
3|	22456|	2
4|	24562|	1


"Orders"테이블의 "PersonID"열이 "Person"테이블의 "PersonID"열을 가리키는 것을 확인하십시오.

"Person"테이블의 "PersonID"열은 "Person"테이블의 PRIMARY KEY입니다.

"주문"테이블의 "PersonID"열은 "주문"테이블의 외래 키입니다.

FOREIGN KEY 제약 조건은 테이블 간의 연결을 파괴하는 작업을 방지하는 데 사용됩니다.

FOREIGN KEY 제약 조건은 또한 가리키는 테이블에 포함 된 값 중 하나 여야하기 때문에 잘못된 데이터가 외부 키 열에 삽입되는 것을 방지합니다.


# CREATE TABLE의 SQL FOREIGN KEY
다음 SQL은 "주문"테이블을 만들 때 "PersonID"열에 FOREIGN KEY를 만듭니다.

**MySQL :**
~~~SQL
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
CREATE TABLE Orders (
    OrderID int NOT NULL PRIMARY KEY,
    OrderNumber int NOT NULL,
    PersonID int FOREIGN KEY REFERENCES Persons(PersonID)
);
~~~

FOREIGN KEY 제약 조건의 이름 지정 및 여러 열의 FOREIGN KEY 제약 조건 정의를 허용하려면 다음 SQL 구문을 사용합니다.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    CONSTRAINT FK_PersonOrder FOREIGN KEY (PersonID)
    REFERENCES Persons(PersonID)
);
~~~
# ALTER TABLE에 대한 SQL FOREIGN KEY

"주문"테이블이 이미 생성 된 경우 "PersonID"열에 FOREIGN KEY 제약 조건을 만들려면 다음 SQL을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
~~~

FOREIGN KEY 제약 조건의 이름 지정 및 여러 열의 FOREIGN KEY 제약 조건 정의를 허용하려면 다음 SQL 구문을 사용합니다.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Orders
ADD CONSTRAINT FK_PersonOrder
FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);
~~~

# FOREIGN KEY 제약 조건 삭제

FOREIGN KEY 제약 조건을 삭제하려면 다음 SQL을 사용하십시오.

**MySQL :**
~~~SQL
ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
ALTER TABLE Orders
DROP CONSTRAINT FK_PersonOrder;
~~~


## SQL CHECK 제약

CHECK 제약 조건은 열에 배치 할 수있는 값 범위를 제한하는 데 사용됩니다.

단일 열에 CHECK 제한 조건을 정의하면이 열에 대해 특정 값만 허용됩니다.

테이블에 CHECK 제한 조건을 정의하면 행의 다른 C 럼에있는 값을 기]으로 특정 C 럼의 값을 제한 할 수 있습니다.

# CREATE TABLE에 대한 SQL CHECK
다음 SQL은 "Person"테이블이 작성 될 때 "Age"C 럼에 CHECK 제한 조건을 작성합니다. CHECK 제약 조건은 18 세 미만의 사람을 가질 수 없도록 보장합니다.

**MySQL :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int CHECK (Age>=18)
);
~~~

CHECK 제약 조건의 이름 지정 및 여러 열에 대한 CHECK 제약 조건 정의를 허용하려면 다음 SQL 구문을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255),
    CONSTRAINT CHK_Person CHECK (Age>=18 AND City='Sandnes')
);
~~~

# ALTER TABLE에 대한 SQL CHECK

테이블이 이미 생성 된 경우 "Age"열에 CHECK 제약 조건을 만들려면 다음 SQL을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD CHECK (Age>=18);
~~~

CHECK 제약 조건의 이름 지정 및 여러 열에 대한 CHECK 제약 조건 정의를 허용하려면 다음 SQL 구문을 사용하십시오.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ADD CONSTRAINT CHK_PersonAge CHECK (Age>=18 AND City='Sandnes');
~~~

# CHECK 제약 조건 삭제

CHECK 제약 조건을 삭제하려면 다음 SQL을 사용하십시오.

**SQL Server / Oracle / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
DROP CONSTRAINT CHK_PersonAge;
~~~
**MySQL :**
~~~SQL
ALTER TABLE Persons
DROP CHECK CHK_PersonAge;
~~~


## SQL DEFAULT 제약 조건

DEFAULT 제약 조건은 열의 기본값을 제공하는 데 사용됩니다.

다른 값을 지정하지 않으면 기본값이 모든 새 레코드에 추가됩니다.

# CREATE TABLE의 SQL DEFAULT

다음 SQL은 "Person"테이블을 만들 때 "City"열의 DEFAULT 값을 설정합니다.

**MySQL / SQL 서버 / 오라클 / MS 액세스 :**
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);
~~~

DEFAULT 제약 조건은 GETDATE ()와 같은 함수를 사용하여 시스템 값을 삽입하는 데에도 사용할 수 있습니다.
~~~SQL
CREATE TABLE Orders (
    ID int NOT NULL,
    OrderNumber int NOT NULL,
    OrderDate date DEFAULT GETDATE()
);
~~~

# ALTER TABLE에 대한 SQL DEFAULT
테이블이 이미 만들어 졌을 때 "도시"열에 DEFAULT 제약 조건을 만들려면 다음 SQL을 사용하십시오.

**MySQL :**
~~~SQL
ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';
~~~

**SQL Server / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ALTER COLUMN City SET DEFAULT 'Sandnes';
~~~
**Oracle:**
~~SQL
ALTER TABLE Persons
MODIFY City DEFAULT 'Sandnes';
~~~

# DEFAULT 제약 조건 삭제

DEFAULT 제약 조건을 삭제하려면 다음 SQL을 사용합니다.

**MySQL :**
~~~SQL
ALTER TABLE Persons
ALTER City DROP DEFAULT;
~~~
**SQL Server / Oracle / MS 액세스 :**
~~~SQL
ALTER TABLE Persons
ALTER COLUMN City DROP DEFAULT;
~~~


## SQL CREATE INDEX 문

CREATE INDEX 문은 테이블에 인덱스를 만드는 데 사용됩니다.

인덱스는 데이터베이스에서 데이터를 매우 빨리 검색하는 데 사용됩니다. 사용자는 색인을 볼 수 없으며 검색 / 쿼리 속도를 높이기 위해 사용됩니다.

**노트** : 색인을 사용하여 테이블을 갱신하는 것은 색인을 갱신해야하기 때.에 표를 갱신하지 않고 시간을 소비합니다. 따라서 자주 검색 할 열에 대해서만 인덱스를 작성하십시오.

# CREATE INDEX 구문
테이블에 인덱스를 만듭니다. 중복 된 값이 허용됩니다.
~~~SQL
CREATE INDEX index_name
ON table_name (column1, column2, ...);
~~~

# CREATE UNIQUE INDEX 구문
테이블에 고유 인덱스를 작성합니다. 중복 값은 허용되지 않습니다.
~~~SQL
CREATE UNIQUE INDEX index_name
ON table_name (column1, column2, ...);
~~~
**참고** : 인덱스를 만드는 구문은 데이터베이스마다 다릅니다. 따라서 데이터베이스의 인덱스 작성 구문을 확인하십시오.


# DROP INDEX 문

DROP INDEX 문은 테이블의 인덱스를 삭제하는 데 사용됩니다.

**MS 액세스 :**
~~~SQL
DROP INDEX index_name ON table_name;
~~~
**SQL Server :**
~~~SQL
DROP INDEX table_name.index_name;
~~~
**DB2 / Oracle :**
~~~SQL
DROP INDEX index_name;
~~~
**MySQL :**
~~~SQL
ALTER TABLE table_name
DROP INDEX index_name;
~~~


## AUTO INCREMENT 필드
자동 증가는 새 레코드가 테이블에 삽입 될 때 고유 번호가 자동으로 생성되도록합니다.

종종 이것은 새로운 레코드가 삽입 될 때마다 자동으로 생성되기를 원하는 기본 키 필드입니다.

# MySQL 구문
다음 SQL 문은 "Person"테이블의 자동 증가 기본 키 필드로 "ID"열을 정의합니다.
~~~SQL
CREATE TABLE Persons (
    ID int NOT NULL AUTO_INCREMENT,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
~~~
MySQL은 AUTO_INCREMENT 키워드를 사용하여 자동 증가 기능을 수행합니다.

기본적으로 AUTO_INCREMENT의 시작 값은 1이며 새 레코드마다 1 씩 증가합니다.

AUTO_INCREMENT 시퀀스를 다른 값으로 시작하려면 다음 SQL 문을 사용하십시오.
~~~SQL
ALTER TABLE Persons AUTO_INCREMENT=100;
~~~

"Persons"테이블에 새 레코드를 삽입하려면 "ID"열에 값을 지정할 필요가 없습니다 (고유 한 값이 자동으로 추가됩니다).
~~~SQL
INSERT INTO Persons (FirstName,LastName)
VALUES ('Lars','Monsen');
~~~
위의 SQL 문은 "Persons"테이블에 새 레코드를 삽입합니다. "ID"열에 고유 한 값이 할당됩니다. "FirstName"열은 "Lars"로 설정되고 "LastName"열은 "Monsen"으로 설정됩니다.

# SQL Server 구문
다음 SQL 문은 "Person"테이블의 자동 증가 기본 키 필드로 "ID"열을 정의합니다.
~~~SQL
CREATE TABLE Persons (
    ID int IDENTITY(1,1) PRIMARY KEY,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
~~~
MS SQL Server는 IDENTITY 키워드를 사용하여 자동 증가 기능을 수행합니다.

위의 예에서 IDENTITY의 시작 값은 1이며 새 레코드마다 1 씩 증가합니다.

**팁** : "ID"열이 값 10에서 시작하여 5 씩 증가하도록 지정하려면 IDENTITY (10,5)로 변경하십시오.

"Persons"테이블에 새 레코드를 삽입하려면 "ID"열에 값을 지정할 필요가 없습니다 (고유 한 값이 자동으로 추가됩니다).
~~~SQL
INSERT INTO Persons (FirstName,LastName)
VALUES ('Lars','Monsen');
~~~
위의 SQL 문은 "Persons"테이블에 새 레코드를 삽입합니다. "ID"열에 고유 한 값이 할당됩니다. "FirstName"열은 "Lars"로 설정되고 "LastName"열은 "Monsen"으로 설정됩니다.

# 액세스 구문
다음 SQL 문은 "Person"테이블의 자동 증가 기본 키 필드로 "ID"열을 정의합니다.
~~~SQL
CREATE TABLE Persons (
    ID Integer PRIMARY KEY AUTOINCREMENT,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
~~~
MS Access는 AUTOINCREMENT 키워드를 사용하여 자동 증가 기능을 수행합니다.

기본적으로 AUTOINCREMENT의 시작 값은 1이며 새 레코드마다 1 씩 증가합니다.

**팁** : "ID"열이 값 10에서 시작하여 5 씩 증가하도록 지정하려면 자동 증가를 AUTOINCREMENT (10,5)로 변경하십시오.

"Persons"테이블에 새 레코드를 삽입하려면 "ID"열에 값을 지정할 필요가 없습니다 (고유 한 값이 자동으로 추가됩니다).
~~~SQL
INSERT INTO Persons (FirstName,LastName)
VALUES ('Lars','Monsen');
~~~
위의 SQL 문은 "Persons"테이블에 새 레코드를 삽입합니다. "P_Id"열에 고유 한 값이 할당됩니다. "FirstName"열은 "Lars"로 설정되고 "LastName"열은 "Monsen"으로 설정됩니다.

# 오라클 구문

오라클에서는 코드가 좀 더 까다 롭습니다.

시퀀스 객체로 자동 증가 필드를 만들어야합니다 (이 객체는 숫자 시퀀스를 생성합니다).

다음 CREATE SEQUENCE 구문을 사용하십시오.
~~~SQL
CREATE SEQUENCE seq_person
MINVALUE 1
START WITH 1
INCREMENT BY 1
CACHE 10;
~~~

위의 코드는 seq_person이라는 시퀀스 객체를 생성합니다. seq_person은 1부터 시작하여 1 씩 증가합니다. 또한 성능을 위해 최대 10 개의 값을 캐시합니다. 캐시 옵션은 더 빠른 액세스를 위해 얼마나 많은 순서 값이 메모리에 저장 될지 지정합니다.

"Persons"테이블에 새 레코드를 삽입하려면 nextval 함수를 사용해야합니다 (이 함수는 seq_person 시퀀스에서 다음 값을 검색합니다).
~~~SQL
INSERT INTO Persons (ID,FirstName,LastName)
VALUES (seq_person.nextval,'Lars','Monsen');
~~~
위의 SQL 문은 "Persons"테이블에 새 레코드를 삽입합니다. "ID"열에는 seq_person 시퀀스의 다음 번호가 할당됩니다. "FirstName"열은 "Lars"로 설정되고 "LastName"열은 "Monsen"으로 설정됩니다.


## SQL DATES

날짜 작업을 할 때 가장 어려운 부분은 삽입하려는 날짜 형식이 데이터베이스의 날짜 열 형식과 일치하는지 확인하는 것입니다.

데이터에 날짜 부분 만 포함되어 있으면 쿼리가 예상대로 작동합니다. 그러나 시간 부분이 관련되면 더 복잡해집니다.

# SQL 날짜 데이터 유형
**MySQL** 에는 데이터베이스에 날짜 또는 날짜 / 시간 값을 저장하기위한 다음 데이터 유형이 있습니다.

* DATE - YYYY-MM-DD 형식
* DATETIME - 형식 : YYYY-MM-DD HH : MI : SS
* TIMESTAMP - 형식 : YYYY-MM-DD HH : MI : SS
* YEAR - YYYY 또는 YY 형식
**SQL Server** 에는 데이터베이스에 날짜 또는 날짜 / 시간 값을 저장하기위한 다음 데이터 형식이 있습니다.

* DATE - YYYY-MM-DD 형식
* DATETIME - 형식 : YYYY-MM-DD HH : MI : SS
* SMALLDATETIME - 형식 : YYYY-MM-DD HH : MI : SS
* TIMESTAMP - 형식 : 고유 번호
**참고** : 데이터베이스에 새 테이블을 만들 때 열에 대해 날짜 유형이 선택됩니다!

# SQL Working with DATES

**관련된 시간 구성 요소가 없으면 두 날짜를 쉽게 비교할 수 있습니다!**

다음의 "주문"테이블이 있다고 가정합니다.

OrderId|	ProductName|	OrderDate
-------|-------------|-----------
1	|Geitost	|2008-11-11
2	|Camembert Pierrot	|2008-11-09
3	|Mozzarella di Giovanni	|2008-11-11
4	|Mascarpone Fabioli	|2008-10-29

이제 우리는 위 표에서 OrderDate가 "2008-11-11"인 레코드를 선택하려고합니다.

다음 SELECT 문을 사용합니다.
~~~SQL
SELECT * FROM Orders WHERE OrderDate='2008-11-11'
~~~

결과 세트는 다음과 같습니다.

OrderId|	ProductName|	OrderDate
1|	Geitost|	2008-11-11
3|	Mozzarella di Giovanni|	2008-11-11
