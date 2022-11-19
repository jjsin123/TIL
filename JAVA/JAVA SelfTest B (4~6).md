# JAVA SelfTest B (4~6)

Author: jk s
Category: JAVA
Created Time: 2022년 11월 19일 오후 3:57
Main Category: Language
Status: 🖨 Published
Tags: SelfTest
Updated Time: 2022년 11월 19일 오후 4:43

## 학습 환경

---

언어 : Java 

IDE : Eclipse

## 문제

---

SelfTest B4

정사각형의 한 변의 길이 n과 종류 m을 입력받은 후 다음과 같은 정사각형 형태로 출력하는 프로그램을 작성하시오.

< 처리조건 >

종류 2번의 경우 숫자의 진행 순서는 처음에 왼쪽에서 오른쪽으로 너비 n만큼 진행 한 후 방향을 바꾸어서 이를 반복한다.

![Untitled](https://user-images.githubusercontent.com/114375741/202840617-fcf88edb-5508-4451-9bd3-bd751079d430.png)

입력형식 : 정사각형 한 변의 길이 n(n의 범위는 100 이하의 정수)과 종류 m(m은 1부터 3사이의 정수)을 입력받는다.

출력형식 : 위에서 언급한 3가지 종류를 입력에서 한 변의 길이 n과 종류 m에 맞춰서 출력한다. 숫자 사이는 공백으로 구분하여 출력한다.

입력 예 :

3 2

출력 예 :

![Untitled 1](https://user-images.githubusercontent.com/114375741/202840621-f183175e-6fc8-4e69-ae26-4d3d0fbb80a7.png)

입력 예 :

4 3

출력 예 :

![Untitled 2](https://user-images.githubusercontent.com/114375741/202840624-a064489e-dcbe-457b-8e31-8c60eae6cd2a.png)

## 코드

---

[https://gist.github.com/jjsin123/2359eafe08be3ec54f4d2017fbc886ad](https://gist.github.com/jjsin123/2359eafe08be3ec54f4d2017fbc886ad)

## 문제

---

SelfTest B5

정사각형의 한 변의 길이 n을 입력받은 후 다음과 같은 문자로 된 정사각형 형태로 출력하는 프로그램을 작성하시오.

< 처리조건 >문자의 진행 순서는 맨 오른쪽 아래에서 위쪽으로 'A'부터 차례대로 채워나가는 방법으로 아래 표와 같이 왼쪽 위까지 채워 넣는다.

'Z' 다음에는 다시 'A'부터 반복된다.

입력형식 : 정사각형 한 변의 길이 n(n의 범위는 1이상 100 이하의 정수)을 입력받는다.

출력형식 : 위의 형식과 같이 한변의 길이가 n인 문자 사각형을 출력한다. 문자 사이는 공백으로 구분하여 출력한다.

입력 예 :

4

출력 예 :

![Untitled 3](https://user-images.githubusercontent.com/114375741/202840626-d366316f-d2b5-49a0-b8e1-4ec70b6074da.png)

## 코드

---

[https://gist.github.com/jjsin123/80b08c0816faa870a76865515afe54fb](https://gist.github.com/jjsin123/80b08c0816faa870a76865515afe54fb)

## 문제

---

SelfTestB6

정사각형의 한 변의 길이 n을 입력받은 후 다음과 같은 문자로 된 정사각형 형태로 출력하는 프로그램을 작성하시오.

< 처리조건 > 문자의 진행 순서는 왼쪽 위에서부터 아래쪽으로 ‘A'부터 차례대로 채워나가고 다시 오른쪽 아래부터 위쪽으로 채워나가는 방법으로 아래 표와 같이 채워 넣는다. 'Z' 다음에는 다시 'A'부터 반복된다.

입력형식 : 정사각형 한 변의 길이 n(n의 범위는 1이상 100 이하의 정수)을 입력받는다.

출력형식 : 위의 형식과 같이 한변의 길이가 n인 문자 사각형을 출력한다. 문자 사이는 공백으로 구분하여 출력한다.

입력 예 : 

4

출력 예 :

![Untitled 4](https://user-images.githubusercontent.com/114375741/202840628-296a9211-9852-4c79-92c4-0ec533a52663.png)

## 코드

---

[https://gist.github.com/jjsin123/e6e39e8490e2ddfbbb632fe5105fa3dc](https://gist.github.com/jjsin123/e6e39e8490e2ddfbbb632fe5105fa3dc)

## 느낀점

---

숫자 사각형과 마찬가지로 배열과 중첩for문을 활용하는 문제들이다. 문자로 변환하기 위해 char를 사용한다.
