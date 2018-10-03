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
