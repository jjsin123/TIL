# Python Numpy 기초

Author: jk s
Category: Python
Created Time: 2022년 11월 19일 오후 3:49
Main Category: Language
Status: 🖨 Published
Tags: 심화, 학습
Updated Time: 2022년 11월 22일 오전 9:34

## 학습 환경

---

Jupyter Notebook, Google Colab

## Numpy란

---

- c언어를 기반으로 내부 반복문을 사용하여 속도가 매우 빠르다.
- 다차원 배열(ndarray)을 편리하게 처리할 수 있도록 지원해주는 파이썬 라이브러리다.

### ndarray와 list 비교

---

- ndarray : 적은 메모리로 데이터를 빠르게 처리하고, 모든 원소는 같은 자료형을 가진다.
- list : 속도가 매우 느리고, 원소가 각각 다른 자료형을 가질 수 있다.

### ndarray

---

- 다차원 배열을 지원한다.
- 서로 다른 타입의 데이터를 담을 수 없다.
- 내부 반복문을 사용해서 속도가 빠르다.
- 배열 간에 산술 연산이 가능하다.
- 데이터 타입 확인 및 변경

`dtype` : 자료형 확인

`astype` : 자료형 변경

- `np.arange`(start, stop, step) : step에 따라 증가하는 수열을 생성한다.
- `reshape` : 만들어진 배열의 데이터를 그대로 가지고 형태를 바꿔준다.
- nan

자료형이 Float형이므로 Integer에서는 오류가 발생한다.

배열에서 연산할 경우 오류가 발생하지 않지만 결과값이 NaN이 된다.

### 연산

---

- 반복문을 사용하지 않아도, 배열의 모든 원소는 반복연산이 사용된다.
- 선형 대수 식을 사용하여 연산 가능하다.

### 차원

---

- 0차원 : Scalar (하나의 데이터 값으로만 존재하는 것)
- 1차원 : Vector (숫자들의 배열 (1D array))
- 2차원 : Matrix (숫자들의 2D array (rows: 행, columns: 열))
- 3차원 이상 : Tensor (숫자들의 다차원 배열)

### 집계함수

---

- `mean` : 평균을 구하는 함수
- `median` : 데이터를 크기로 정렬하고 그 중 가운데 수 출력하는 함수
※ 만약 데이터 개수가 짝수일 경우 가장 가운데의 두 수의 평균을 구한다.
- `var` : 분산 구하는 함수
- `std` : 표준편차 구하는 함수
- `sum` : 합계 구하는 함수
- `max` : 가장 큰 수를 구하는 함수
- `min` : 가장 작은 수를 구하는 함수