# JAVA SelfTest B (1~3)

Author: jk s
Category: JAVA
Created Time: 2022년 11월 19일 오후 3:55
Main Category: Language
Status: 🖨 Published
Tags: SelfTest
Updated Time: 2022년 11월 19일 오후 4:17

## 학습 환경

---

언어 : Java 

IDE : Eclipse

## 문제

---

SelfTest B1

사각형의 높이 n과 너비 m을 입력받은 후 n행 m열의 사각형 형태로 1부터 n*m번까지 숫자가 차례대로 출력되는 프로그램을 작성하시오.

입력형식 : 사각형의 높이n와 너비m(n과 m의 범위는 100이하의 정수)을 입력받는다.

출력형식 : 위에서 형태의 직사각형을 입력에서 들어온 높이 n과 너비 m에 맞춰서 출력한다. 숫자 사이는 공백으로 구분한다.

입력 예 :

4 5

출력 예 :

1 2 3 4 5
6 7 8 9 10
11 12 13 14 15
16 17 18 19 20

## 코드

---

[https://gist.github.com/jjsin123/264361fedb728449ca4e1f97f6b2d4fa](https://gist.github.com/jjsin123/264361fedb728449ca4e1f97f6b2d4fa)

## 문제

---

SelfTest B2

사각형의 높이 n과 너비 m을 입력받은 후 사각형 내부에 지그재그 형태로 1부터 n*m번까지 숫자가 차례대로 출력되는 프로그램을 작성하시오. <처리조건>숫자의 진행 순서는 처음에 왼쪽에서 오른쪽으로 너비 m만큼 진행 한 후 방향을 바꾸어서 이를 반복한다.

![Untitled](JAVA%20SelfTest%20B%20(1~3)%209d65529aaf424bfab769af5e96354165/Untitled.png)

입력형식 : 사각형의 높이n와 너비m(n과 m의 범위는 100이하의 정수)을 입력받는다.

출력형식 : 위에서 형태의 직사각형을 입력에서 들어온 높이 n과 너비 m에 맞춰서 출력한다. 숫자 사이는 공백으로 구분한다.

입력 예 : 

4 5

출력 예 :

1 2 3 4 5
10 9 8 7 6
11 12 13 14 15
20 19 18 17 16

## 코드

---

[https://gist.github.com/jjsin123/009b3b7deb590c5cb7c6b5bc002ad2c4](https://gist.github.com/jjsin123/009b3b7deb590c5cb7c6b5bc002ad2c4)

## 문제

---

SelfTestB3

정사각형의 한 변의 길이 n을 입력받은 후 다음과 같이 숫자로 된 정사각형 형태로 출력하는 프로그램을 작성하시오. <처리조건> 숫자의 진행 순서는 처음에 왼쪽 위에서 아래쪽으로 n만큼 진행 한 후 바로 오른쪽 위에서 다시 아래쪽으로 진행하는 방법으로 정사각형이 될 때까지 반복한다.

입력형식 : 정사각형 한 변의 길이 n(n의 범위는 100이하의 정수)을 입력받는다.

출력형식 : 위의 형식과 같이 한 변의 길이가 n인 숫자 사각형을 출력한다.  숫자 사이는 공백으로 구분한다.

![Untitled](JAVA%20SelfTest%20B%20(1~3)%209d65529aaf424bfab769af5e96354165/Untitled%201.png)

입력 예 :

4

출력 예 :

1 5 9 13
2 6 10 14
3 7 11 15
4 8 12 16

## 코드

---

[https://gist.github.com/jjsin123/810cb3cdbfc8e9fbb8a5d8555087f290](https://gist.github.com/jjsin123/810cb3cdbfc8e9fbb8a5d8555087f290)

## 느낀점

---

배열과 중첩 for문을 적절하게 활용하는 기본 문제들이다. B1 문제는 기본 배열, B2는 지그재그, B3은 세로로 출력이 가능한지를 물어보는 문제이다.