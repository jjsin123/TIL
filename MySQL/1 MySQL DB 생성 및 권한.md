# 1. MySQL DB 생성 및 권한

Author: jk s
Category: MySQL
Created Time: 2022년 12월 24일 오전 12:50
Main Category: DataBase
Tags: 기본, 학습
Updated Time: 2022년 12월 25일 오전 12:21

**SQL(Structured Query Language)**

- SQL은 데이터를 보다 쉽게 검색하고 추가, 삭제, 수정 같은 조작을 할 수 있도록 고안된 컴퓨터 언어이다.
- 관계형 데이터베이스에서 데이터를 조작하고 쿼리하는 표준 수단이다.
- DML (Data Manipulation Language): 데이터를 조작하기 위해 사용한다. INSERT, UPDATE, DELETE, SELECT 등이 여기에 해당한다.
- DDL (Data Definition Language): 데이터베이스의 스키마를 정의하거나 조작하기 위해 사용한다. CREATE, DROP, ALTER 등이 여기에 해당한다.
- DCL (Data Control Language) : 데이터를 제어하는 언어이다. 권한을 관리하고, 테이터의 보안, 무결성 등을 정의합니다.GRANT, REVOKE 등이 여기에 해당한다.

**Database 생성하기**

콘솔에서 다음과 같이 명령을 실행한다.

MySQL 관리자 계정인 root로 데이터베이스 관리 시스템에 접속하겠다는 것이다.

```
mysql –uroot  -p
```

window 사용자는 설치 시에 입력했던 암호를 입력한다.

![image](https://user-images.githubusercontent.com/114375741/209466382-347a0f40-9e2a-4f19-bbb1-745c652e0331.png)


관리자 계정으로 MySQL에 접속했다면, 다음과 같은 명령으로 데이터베이스를 생성한다.

```
create database DB이름;
```

**Database 사용자 생성과 권한 주기**

- Database를 생성했다면, 해당 데이터베이스를 사용하는 계정을 생성해야 한다.
- 또한, 해당 계정이 데이터베이스를 이용할 수 있는 권한을 줘야 한다.
- 아래와 같은 명령을 이용해서 사용자 생성과 권한을 줄 수 있다.
- db이름 뒤의 * 는 모든 권한을 의미한다.
- @’%’는 어떤 클라이언트에서든 접근 가능하다는 의미이고, @’localhost’는 해당 컴퓨터에서만 접근 가능하다는 의미이다.
- flush privileges는 DBMS에게 적용을 하라는 의미이다.
- 해당 명령을 반드시 실행해줘야 한다.

```
grant all privileges on db이름.* to 계정이름@'%' identified by ＇암호’;
grant all privileges on db이름.* to 계정이름@'localhost' identified by ＇암호’;
flush privileges;
```

- 사용자 계정이름은 'connectuser', 암호는 'connect123!@#', 해당 사용자가 사용하는 데이터베이스는 'connectdb'로 계정을 생성하려면 다음과 같이 명령을 수행한다.

```
CREATE USER connectuser@localhost IDENTIFIED BY 'connect123!@#';

GRANT ALL PRIVILEGES ON connectdb.* TO 'connectuser'@'localhost';

FLUSH PRIVILEGES:
```

**MySQL 연결끊기**

프롬프트에서 quit혹은 exit라고 입력한다.

```
mysql> QUIT
mysql> exit
```

Bye라고 나오면 연결 끊기 성공

**MySQL 버전과 현재 날짜 구하기**

```
SELECT VERSION(), CURRENT_DATE;
```

**키워드는 대소문자를 구별하지 않는다.**

다음 쿼리들은 모두 같다.

```
mysql> SELECT VERSION(), CURRENT_DATE;
mysql> select version(), current_date;
mysql> SeLeCt vErSiOn(), current_DATE;
```

**쿼리를 이용해서 계산식의 결과도 구할 수 있다.**

함수 및 수식 사용 예제

```
mysql> SELECT SIN(PI()/4), (4+1)*5;
+-------------+---------+
| SIN(PI()/4) | (4+1)*5 |
+-------------+---------+
|    0.707107 |      25 |
+-------------+---------+
```

**여러 문장을 한 줄에 연속으로 붙여서 실행가능하다.**

각 문장에 semicolon(;)만 붙혀 주면 된다.

```
mysql> SELECT VERSION(); SELECT NOW();
+--------------+
| VERSION()    |
+--------------+
| 3.22.20a-log |
+--------------+
+---------------------+
| NOW()               |
+---------------------+
| 2004 00:15:33 |
+---------------------+
```

**하나의 SQL은 여러 줄로 입력가능하다.**

MySQL은 문장의 끝을 라인으로 구분하는 것이 아니라 semicolon(;)으로 구분하기 때문에 여러 줄에 거쳐 문장을 쓰는 것도 가능하다.

```
mysql> SELECT
    -> USER()
    -> ,
    -> CURRENT_DATE;
+--------------------+--------------+
| USER()             | CURRENT_DATE |
+--------------------+--------------+
| joesmith@localhost | 1999-03-18   |
+--------------------+--------------+
```

**SQL을 입력하는 도중에 취소할 수 있다.**

긴 쿼리를 작성하다가 중간에 취소해야 하는 경우에는 즉시 \c를 붙혀주면 된다.

```
SELECT

-> USER()

-> \c

mysql>
```

**DBMS에 존재하는 데이터베이스 확인하기**

작업하기 위한 데이터베이스를 선택하기 위해서는 어떤 데이터베이스가 존재하는지 알아보아야 한다.

현재 서버에 존재하는 데이터베이스를 찾아보기 위해서 SHOW statement을 사용한다.

```
show databases;
+-----------------------+
| Database               |
+-----------------------+
| information_schema |
| connectdb              |
+-----------------------+
2 rows in set (0.00 sec)
```

**사용중인 데이터베이스 전환하기**

Database을 선택하기 위해,  “use” command 사용한다.

```
use mydb;
```

데이터베이스를 전환하려면, 이미 데이터베이스가 존재해야 하며 현재 접속 중인 계정이 해당 데이터베이스를 사용할 수 있는 권한이 있어야 한다.
