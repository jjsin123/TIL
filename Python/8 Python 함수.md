# 8. Python 함수

Author: jk s
Category: Python
Created Time: 2022년 11월 18일 오전 10:19
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 18일 오후 12:02

## 함수 기본

---

### 함수 개념

---

- 특정 값을 인자로 받고, 결과값을 반환
- 함수가 필요할 때마다 호출 가능
- 코드의 캡슐화(Capsulation)
- 중복되는 소스 코드를 최소화
- 소스 코드의 재 사용성을 높임

### 함수 선언

---

**함수 선언 문법**

```python
# 파이썬 함수 기본 구조
def 함수명(매개변수):
    <수행문>
    return <반환값>

# 매개변수와 인수
def add(a, b):  # a, b는 매개변수
    return a+b

print(add(3, 4))  # 3, 4는 인수
```

- def : 정의(definition)의 줄임으로 사용
- 함수 명 : 사용자가 임의로 지정
- 매개변수(parameter) : 함수에서 입력 값으로 사용하는 변수
- 반환 값 : 함수에서 반환할 결과 값 지정

**매개 변수와 반환 값이 없는 함수**

- 함수에 매개변수와 반환 값이 없이 사용 가능
- 함수를 호출하면 함수의 수행문이 실행

```python
def my_function_1():
    print("hello")

my_function_1()
# hello
```

**매개변수만 있는 함수**

- 문자열 매개변수를 사용한 함수

```python
def hello(string):
  print("Hello", string)
  
hello("Python")
# Hello Python
```

**반환 값만 있는 함수**

- 문자열 반환 값을 사용한 함수

```python
def my_function_1(x):
    print('hello'+str(x))
    
my_function_1('jjsin123')
#hellojjsin123
```

**매개변수와 반환 값이 있는 함수**

```python
# 정수형 매개변수와 반환 값을 사용한 함수
# 예제1
def square(num):
  return num * num
square(5)
# 25

# 예제2
def my_fn_add_10(x):
    y=x+10
    print('function y = ' + str(y))
    return y
 
y=5
val = my_fn_add_10(y)
print('out side y =' +str(y)) #여기 y는 윗문단의 y와 다른 값이다.
'''
function y = 15
out side y =5
'''
```

**매개변수가 여러개 있는 함수**

- 정수형 매개변수 여러개를 사용한 함수
- 매개변수를 지정하여 호출 가능

```python
def add(n1, n2):
  return n1 + n2
print(add(5, 8))
#13
```

**키워드 매개변수**

- 함수의 매개변수를 변수명을 지정하여 호출 가능

```python
def add(n1, n2):
  return n1 + n2
print(add(n2 = 5, n1 = 8)) # 변수 지정
# 13
```

**가변 매개변수**

- 매개변수가 몇 개인지 알 수 없을 때 사용
- 매개변수 앞에 * 을 표시

```python
def sum(*args):
  result = 0
  for i in args:
    result = result + i
  return result
print(sum(1, 2, 3))
print(sum(1, 2, 3, 4, 5))

'''
6
15
'''
```

**여러 반환 값이 있는 함수**

- 함수의 반환 값은 하나
- 여러 반환 값을 사용할 경우 튜플 형태로 반환한다.

```python
def plus_and_minus(n1, n2):
  return n1 + n2, n1 - n2

result = plus_and_minus(8, 5)
print(result)
result1, result2 = plus_and_minus(8, 5)
print(result1, result2)
'''
(13,3)
13 3
'''
```

### 함수 심화

---

**내부 함수**

- 함수 안에 함수가 존재
- 내부 함수는 외부에서 호출 불가

```python
def func1(n1, n2):
  def func2(num1, num2):
    return num1 + num2
  return func2(n1, n2)
print(func1(5, 8))
#13
```

**재귀 함수**

- 함수가 자기 자신을 다시 부르는 함수
- `count()` 함수 내부에서 `count()` 함수를 호출

```python
def count(n):
  if n >= 1:
    print(n, end=' ')
    count(n - 1)
  else:
    return
count(10)
# 10 9 8 7 6 5 4 3 2 1
```

**람다 함수**

- 함수를 한 줄로 간결하게 만들어 사용

```python
# 기본 함수
def add(n1, n2):
  return n1 + n2
print(add(5, 8))
# 13

# 람다 함수
add2 = lambda n1, n2 : n1 + n2
print(add2(5, 8))
# 13
```