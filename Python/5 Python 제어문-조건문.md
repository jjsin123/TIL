# 5. Python 제어문-조건문

Author: jk s
Category: Python
Created Time: 2022년 11월 17일 오전 11:01
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 17일 오후 1:22

## 조건문

---

- 조건에 따라 문장을 수행
- 파이썬에서 제공하는 조건문 `if`, `else`, `elif`

### if 문

---

- if문은 True와 False를 판단하는 조건문
- if 조건 뒤에는 콜론(:)

```python
# if 기본 문법
if <조건>:
	<문장>
```

```python
# 기본 if 예제
if True:
	print("Hello World")
''' 실행 결과
Hello World
'''

pm = 40
if pm > 35:
	print("미세먼지 농도: 나쁨")
''' 실행 결과
미세먼지 농도: 나쁨
'''
```

### if-else 문

---

```python
# if-else 기본 문법
if <조건>:
 <문장 1>
else:
 <문장 2>
```

```python
# if-else 예제
pm = 30
if pm >= 36:
	print("미세먼지 농도: 나쁨")
else:
	print("미세먼지 농도: 좋음")
''' 실행 결과
미세먼지 농도: 좋음
'''

pocket = ['paper', 'cellphone', 'money']
if 'money' in pocket:
	print("택시를 타고 가라")
else:
	print("걸어가라")
''' 실행 결과
택시를 타고 가라
'''
```

### if-elif-else 문

---

```python
# if-elif-else 기본 문법
if <조건>:
 <문장 1>
elif <조건>:
 <문장 2>
else:
 <문장 3>
```

![Untitled](5%20Python%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20a2b429a93e844ef89a8dad7ef23b1ae5/Untitled.png)

```python
# if-elif-else 예제
pm = 40
if pm < 16:
	print("미세먼지 농도: 좋음")
elif pm < 36:
	print("미세먼지 농도: 보통")
elif pm < 76:
	print("미세먼지 농도: 나쁨")
else:
	print("미세먼지 농도: 매우나쁨")
''' 실행 결과
미세먼지 농도: 나쁨
'''
```

### 중첩 if 문

---

- if 문 안에 if 문이 포함된 형태

![Untitled](5%20Python%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20a2b429a93e844ef89a8dad7ef23b1ae5/Untitled%201.png)

```python
# 중첩 if 예제
pocket = ['paper', 'handphone']
card = True
if 'money' in pocket:
	print("택시를 타고가라")
else:
	if card:
		print("택시를 타고가라")
	else:
		print("걸어가라")
''' 실행 결과
택시를 타고 가라
'''
```

### if-pass 문

---

- 조건문은 있지만 실행할 문장이 없는 경우, 오류가 발생하지 않도록 무시하고 넘어가는 기능

```python
# if-pass 예제
for x in range(5):
	pass
x=1
if True:
	pass
x=1
def my_fun():
	pass
```

### if 조건 연산자

---

- 비교 연산자 : `<`  , `>` , `==` , `!=` , `>=` , `<=`

```python
# 비교 연산자 예제
if 2 > 1:
	print(2)
if 3 == 3:
	print(3)
if 1 != 2:
	print(1
'''
2
3
1
'''
```

- 논리 연산자 : `and` , `or` , `not`

```python
# 논리 연산자 예제
rain = True
snow = True
sun = False
if rain and snow:
	print("진눈깨비")
if not sun:
	print("흐림")
else:
	print("맑음")
'''
진눈깨비
흐림
'''
```

- 멤버 연산자 : `in` , `not in`

```python
# 멤버 연산자 예제
list = ['One', 'Two', 'Three']
if 'One' in list:
	print('One')
if 'Four' not in list:
	print('No')
'''
One
No
'''
```

- 식별 연산자 : `is` , `is not`

```python
# 식별 연산자 예제
if 'One' is 'One':
	print('One')
if 'One' is not 'Two':
	print('One is not Two')
'''
One
One is not Two
'''
```

### 조건부 표현식

---

- 한 라인으로 조건식을 사용한 표현

```python
# 조건부 표현식 예제
score = 75
msg = "통과" if score >= 70 else "탈락"
print(msg)
'''
통과
'''
```