# 2. MySQL 테이블

Author: jk s
Category: MySQL
Created Time: 2022년 12월 24일 오전 1:30
Main Category: DataBase
Tags: 기본, 학습
Updated Time: 2022년 12월 25일 오후 5:19

**데이터를 저장하는 공간 테이블(Table)**

- 마이크로소프트의 엑셀(Excel)을 실행하면 표가 나온다. 이러한 표에 각종 값을 저장할 수 있다.
- 데이터베이스도 엑셀의 표와 유사한 테이블을 가질 수 있다.
- 엑셀과 다른 점은 데이터베이스를 생성해도 테이블은 존재하지 않는다는 것이다.
- 테이블을 사용하려면 테이블을 생성하는 SQL을 사용해야 한다.
- 그리고, 테이블에 값을 저장하려면 저장하기 위한 SQL을 사용해야 한다.

![2_8_1_(table)_.png](2%20MySQL%20%E1%84%90%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%87%E1%85%B3%E1%86%AF%205269f2f8adf44a48bda6875bbeacade7/2_8_1_(table)_.png)

**테이블(table)의 구성요소**

- 테이블 : RDBMS의 기본적 저장구조 한 개 이상의 column과 0개 이상의 row로 구성한다.
- 열(Column) : 테이블 상에서의 단일 종류의 데이터를 나타냄. 특정 데이터 타입 및 크기를 가지고 있다.
- 행(Row) : Column들의 값의 조합. 레코드라고 불림. 기본키(PK)에 의해 구분. 기본키는 중복을 허용하지 않으며 없어서는 안 된다.
- Field : Row와 Column의 교차점으로 Field는 데이터를 포함할 수 있고 없을 때는 NULL 값을 가지고 있다.

**현재 데이터베이스에 존재하는 테이블 목록 확인하기**

Database를 선택 후, Database의 전체 테이블 목록을 출력한다.

```
mysql> show tables;

Empty set (0.02 sec)
```

“empty set” 은  데이터베이스에 어떤 테이블도 아직 생성되지 않았다는 것을 알려준다.

**SQL 연습을 위한 테이블 생성과 값의 저장**

미리 준비된 examples.sql로 실습을 진행한다. 

[examples.sql](2%20MySQL%20%E1%84%90%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%87%E1%85%B3%E1%86%AF%205269f2f8adf44a48bda6875bbeacade7/examples.sql)

터미널에서 examples.sql이 있는 폴더로 이동한 후, 다음과 같이 명령을 수행한다.

명령을 수행한 후 암호를 입력한다.

```
mysql   -uconnectuser  -p
-> password입력

mysql   -uconnectuser  -p  connectdb   <  examples.sql
```

examples.sql에는 연습을 위한 테이블 생성문과 해당 테이블에 값을 저장하는 입력문이 존재한다.

```
mysql –uconnectuser -p  connectdb
```

위의 명령으로 connectdb에 접속한 후 다음과 같이 명령을 수행한다.

```
show tables;
```

위의 명령은 접속한 db의 테이블 목록을 보는 명령이다.

![https://cphinf.pstatic.net/mooc/20180131_157/1517366408574LmBpS_PNG/2_8_1_SQL_____.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_157/1517366408574LmBpS_PNG/2_8_1_SQL_____.png?type=w760)

**테이블 구조를 확인하기 위한 DESCRIBE 명령**

table 구조를 확인하기 위해,  DESCRIBE 명령을 사용할 수 있다.

짧게 DESC라고 사용해도 된다.

EMPLOYEE테이블의 구조를 확인해 본다.

```
mysql> desc EMPLOYEE;
```