# 2. Python 문자열

Author: jk s
Category: Python
Created Time: 2022년 11월 16일 오전 11:49
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 16일 오후 2:16

## 문자열(String)

---

- 문자, 단어 등으로 구성된 문자들의 집합
- 파이썬에서 문자열은 작은따옴표(') 또는 큰 따옴표(")로 표현
- 이스케이프 문자`\n`를 이용하여 여러 줄이 있는 문자열 생성 가능

```python
text = "동해물과 백두산이 마르고 닳도록\n하느님이 보우하사 우리나라 만세\n무궁화 삼천리 화려강산\n대한사람, 대한으로 길이 보전하세."
print(text)

''' 출력결과
동해물과 백두산이 마르고 닳도록
하느님이 보우하사 우리나라 만세
무궁화 삼천리 화려강산
대한 사람, 대한으로 길이 보전하세.
'''
```

- 작은 따옴표 3개 또는 큰 따옴표 3개를 이용하여 여러 줄이 있는 문자열 생성

```python
text = """동해물과 백두산이 마르고 닳도록
하느님이 보우하사 우리나라 만세.
무궁화 삼천리 화려강산
대한 사람, 대한으로 길이 보전하세."""
print(text)

''' 출력결과
동해물과 백두산이 마르고 닳도록
하느님이 보우하사 우리나라 만세
무궁화 삼천리 화려강산
대한 사람, 대한으로 길이 보전하세.
'''
```

## 문자열 연산(String Operators)

---

```python
# 문자열 더하기
s1 = '동해물과'
s2 = "백두산이"
print(s1 + s2)

# 결과 : 동해물과백두산이

# 문자열 곱하기
s = "String "
print(s * 3)
# 결과 : String String String

# 문자열 길이 len()함수 이용
s = "String "
print(len(s))
print(len(s * 3))

# 결과 : 7
# 결과 : 21
```

## 문자열 인덱싱(indexing)

---

- 문자열은 리스트처럼 문자 하나하나가 상대적인 주소(offset)를 가진다.
- 이 주소를 사용해 할당된 값을 가져오는 인덱싱을 사용

```python
s = "String"
print(s)
print(s[-6])
print(s[-5])
print(s[-4])
print(s[-3])
print(s[-2])
print(s[-1])

''' 결과값
String
S
t
r
i
n
g
'''
```

## 문자열 슬라이싱(slicing)

---

- 문자열의 주소를 이용하여 문자열을 조각(부분)을 추출

```python
s = "CentumLab - Centum Computer Laboratory"
print(s)
print(s[0:7])
print(s[:7])
print(s[10:])
print(s[-10:])
print(s[-19:-11])

''' 결과값
CentumLab - Centum Computer Laboratory
CentumL
CentumL
- Centum Computer Laboratory
Laboratory
Computer
'''
```

## 내장 문자열 함수

---

`capitalize()` : 첫 문자가 대문자인 문자열로 변환

`casefold()` : 모든 문자가 소문자인 문자열로 변환

`count()` : 문자열에 포함된 ' ' 문자의 갯수를 반환

`find()` : 문자열에서 문자 ' '의 해당 위치 반환

`rfind()` :문자열에서 문자 ' '를 해당 위치를 오른쪽부터 탐색하여 가장 큰 인덱스를 반환

`index()` : 문자열에서 문자 ' '의 해당 위치 반환

`rindex()` : 문자열에서 문자 ' '를 해당 위치를 오른쪽부터 탐색하여 가장 큰 인덱스를 반환

`isalnum()` : 문자열에 알파벳이나 숫자가 1개 이상 있으면 True 반환

`isalpha()` : 문자열에 알파벳이 1개 이상 있으면 True 반환

`isdecimal()` : 문자열의 모든 문자가 10진수 문자이면 True 반환

`isdigit()` : 문자열의 모든 문자가 숫자일 때 True 반환

`isnumeric()` : 문자열의 모든 문자가 수치형일 때 True 반환

`isspace()` : 문자열 내에 공백 문자가 있으면 True 반환

`istitle()` : 첫 글자가 대문자이면 True 반환

`islower()` : 모든 문자가 소문자이면 True 반환

`isupper()` : 모든 문자가 대문자이면 True 반환

`join()` : 공백 문자 ' '를 문자 사이마다 추가한 문자열 반환

`center()` / `ljust()` / `rjust()` :

가운데, 왼쪽, 오른쪽 정렬

`lower()` / `upper()` / `title()` / `swapcase()` :

소문자, 대문자, 첫 문자만 대문자, 대문자는 소문자로 소문자는 대문자로 반환

`strip()` / `lstrip()` / `rstrip()` :

양쪽, 왼쪽, 오른쪽 공백 제거

`partition()` / `rpartition()` :

문자 ‘ ‘기준, 마지막 문자 ‘ ‘ 기준으로 분할

`replace()` : 특정 문자를 교체

`split()` / `rsplit()` / `splitlines()` : 구분

문자열을 기본 구분자, 구분자 “, 구분자 ‘_’ 을 이용하여 구분

`startswith()` / `endswith()` : 

문자열에서 시작문자, 마지막 문자를 확인

## 문자열 포맷팅

---

**f 문자열 포맷팅**

- 문자열 포맷팅을 위해 새롭게 나온 기능으로 문자열 앞에 f를 붙여서 구분
- 변수 s와 n에 대해서 문자열에 포함된 이름으로 매핑하여 사용 가능

```python
s = "사과"
n = 2
print(f"나는 사과가 {n}개 있다.")
print(f"나는 {s}가 {n}개 있다.")

# 나는 사과가 2개 있다.
# 나는 사과가 2개 있다.
```