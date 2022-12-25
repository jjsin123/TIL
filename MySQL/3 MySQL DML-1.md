# 3. MySQL DML-1

Author: jk s
Category: MySQL
Created Time: 2022년 12월 24일 오후 5:14
Main Category: DataBase
Tags: 기본, 학습
Updated Time: 2022년 12월 25일 오전 12:23

**데이터 조작어(Data Manipulation Language, DML)의 종류**

데이터 조작어는 모두 동사로 시작한다.

시작하는 동사에 따라서 다음과 같은 4가지 조작어가 있다.

- SELECT – 검색
- INSERT - 등록
- UPDATE - 수정
- DELETE - 삭제

**SELECT 구문의 기본문형**

![https://cphinf.pstatic.net/mooc/20180131_187/1517374752273Ba8n9_PNG/2_8_2_select__.PNG?type=w760](https://cphinf.pstatic.net/mooc/20180131_187/1517374752273Ba8n9_PNG/2_8_2_select__.PNG?type=w760)

**SELECT 구문 예제(전체 데이터 검색)**

- 전체 데이터 검색
- SELECT 뒤에 * 를 기술함으로써 나타낼 수 있다.

예제 : departments 테이블의 모든 데이터를 출력하시오.

```
SELECT * FROM  DEPARTMENT;
```

![https://cphinf.pstatic.net/mooc/20180131_204/15173752726665yfHB_PNG/2_8_2_select__.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_204/15173752726665yfHB_PNG/2_8_2_select__.png?type=w760)

**SELECT 구문 예제(특정 컬럼 검색)**

- SELECT 뒤에 컬럼을 콤마(,)로 구별해서 나열

예제 : employee 테이블에서 직원의 사번(empno), 이름(name), 직업(job)을 출력하시오.

어떤 칼럼이 있는지는 desc명령으로 확인

```
select empno, name, job from employee;
```

![https://cphinf.pstatic.net/mooc/20180131_242/1517375406686GtLK0_PNG/2_8_2_select__%28__%29.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_242/1517375406686GtLK0_PNG/2_8_2_select__%28__%29.png?type=w760)

**SELECT 구문 예제(컬럼에 Alias부여하기)**

- 컬럼에 대한 ALIAS(별칭)을 부여해서 나타내는 칼럼의 HEADING을 변경할 수 있다.

예제 : employee 테이블에서 직원의 사번(empno), 이름(name), 직업(job)을 출력하시오.

```
select empno as 사번, name as 이름, job as 직업 from employee;
```

![https://cphinf.pstatic.net/mooc/20180131_241/1517375599282HCWV3_PNG/2_8_2_select__%28_alias%29.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_241/1517375599282HCWV3_PNG/2_8_2_select__%28_alias%29.png?type=w760)

**SELECT 구문 예제(컬럼의 합성(Concatenation))**

- 문자열 결합함수 concat 사용

예제 : employee 테이블에서 사번과 부서번호를 하나의 칼럼으로 출력하시오.

```
SELECT concat( empno, '-', deptno) AS '사번-부서번호'
FROM employee;
```

![https://cphinf.pstatic.net/mooc/20180131_100/1517375714196vQgJz_PNG/2_8_2_select__%28_%29.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_100/1517375714196vQgJz_PNG/2_8_2_select__%28_%29.png?type=w760)

**SELECT 구문 예제(중복행의 제거)**

- 중복되는 행이 출력되는 경우, DISTINCT 키워드로 중복행을 제거

예제1 : 사원 테이블의 모든 부서번호 출력하시오. (사원 수 만큼 출력된다.)

```
select deptno from employee;
```

![https://cphinf.pstatic.net/mooc/20180131_181/1517375842547vAATO_PNG/2_8_2_select__%28_%29.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_181/1517375842547vAATO_PNG/2_8_2_select__%28_%29.png?type=w760)

예제2 : 사원 테이블의 부서번호를 중복되지 않게 출력하시오.

```
select distinct deptno from employee;
```

![https://cphinf.pstatic.net/mooc/20180131_259/1517375862194IANYL_PNG/2_8_2_select__%28_%29-2.png?type=w760](https://cphinf.pstatic.net/mooc/20180131_259/1517375862194IANYL_PNG/2_8_2_select__%28_%29-2.png?type=w760)

**SELECT 구문 예제(정렬하기)**

![https://cphinf.pstatic.net/mooc/20180227_237/15196955203980m2pE_PNG/2.PNG?type=w760](https://cphinf.pstatic.net/mooc/20180227_237/15196955203980m2pE_PNG/2.PNG?type=w760)

예제 : employee 테이블에서 직원의 사번(empno), 이름(name), 직업(job)을 출력하시오.

단, 이름을 기준으로 오름차순 정렬한다.

```
select empno, name, job from employee order by name;

select empno as 사번, name as 이름, job as 직업 from employee order by 이름;
```

예제 : employee 테이블에서 직원의 사번(empno), 이름(name), 직업(job)을 출력하시오.

단, 이름을 기준으로 내림차순 정렬한다.

```
select empno, name, job from employee order by name desc;
```