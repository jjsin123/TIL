# 10. Python 모듈

Author: jk s
Category: Python
Created Time: 2022년 11월 18일 오후 9:41
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 21일 오후 9:17

## 모듈(Module)

---

- 함수, 변수 그리고 클래스의 집합
- 다른 파이썬 프로그램에서 가져와 사용할 수 있는 파이썬 파일

### 모듈의 종류

---

- 사용자 정의 모듈 : 사용자가 직접 정의해서 사용하는 모듈
- 표준 모듈 : 파이썬에서 기본 제공하는 모듈
- 서드 파티 모듈 :  외부에서 제공하는 모듈
    - 파이썬 표준 모듈에 모든 기능이 있지 않음
    - 서드 파티 모듈을 이용해 고급 프로그래밍 가능
    - 게임 개발을 위한 pygame, 데이터베이스 기능의 SQLAlchemy, 데이터 분석 기능의 NumPy, Pandas

### 사용자 정의 모듈

---

- 사용자가 사용할 모듈을 직접 정의
- 모듈 이름으로 파일명을 사용
- IPython(Colab 환경) 내장 매직 명령어(magic command) 사용
    - %%writefile : 셀의 코드를 .py 파이썬 코드 파일로 저장
    - %load : 파이썬 코드 파일 불러오기
    - %run : 파이썬 코드 파일 실행

```python
%%writefile Module.py
def func1():
  print("Module.py: func1()")
def func2():
  print("Module.py: func2()")
def func3():
  print("Module.py: func3()")
# Writing Module.py
```

```python
!ls
# Module.py  sample_data
```

```python
%load Module.py
```

```python
%run Module.py
```

```python
import Module
Module.func1()
Module.func2()
Module.func3()
'''
Module.py: func1()
Module.py: func2()
Module.py: func3()
'''
```

### 파이썬 표준 모듈

---

- 파이썬에서 기본으로 내장된 유용한 속성과 함수들이 많음

```python
import sys
print(sys.builtin_module_names)
# ('_abc', '_ast', '_bisect', '_blake2', '_codecs', '_collections', '_datetime', '_elementtree', '_functools', '_heapq', '_imp', '_io', '_locale', '_md5', '_operator', '_pickle', '_posixsubprocess', '_random', '_sha1', '_sha256', '_sha3', '_sha512', '_signal', '_socket', '_sre', '_stat', '_string', '_struct', '_symtable', '_thread', '_tracemalloc', '_warnings', '_weakref', 'array', 'atexit', 'binascii', 'builtins', 'cmath', 'errno', 'faulthandler', 'fcntl', 'gc', 'grp', 'itertools', 'marshal', 'math', 'posix', 'pwd', 'pyexpat', 'select', 'spwd', 'sys', 'syslog', 'time', 'unicodedata', 'xxsubtype', 'zipimport', 'zlib')
```

### 시간 모듈**(datetime)**

---

- 운영체제가 제공하는 시간 기능을 파이썬에서 사용할 수 있도록 만들어진 모듈
- 시간 모듈을 사용하기 위해서는 `import time` 필요

```python
# 시간모듈 time 예제
import time
print(time)
print(time.time())
print(time.time())
print(time.time())
now = time.gmtime(time.time())  # 현재시간   tm_isdst - 서머타임 유무
print(now)
year = str(now.tm_year)
month = str(now.tm_mon)
day = str(now.tm_mday)
print(year + "년", month + "월", day + "일")
hour = str(now.tm_hour)
minute = str(now.tm_min)
sec = str(now.tm_sec)
print(hour + "시", minute + "분", sec + "초")

'''
<module 'time' (built-in)>
1665917205.9058754
1665917205.9068325
1665917205.9074557
time.struct_time(tm_year=2022, tm_mon=10, tm_mday=16, tm_hour=10, tm_min=46, tm_sec=45, tm_wday=6, tm_yday=289, tm_isdst=0)
2022년 10월 16일
10시 46분 45초
'''
```

### 랜덤 모듈**(random)**

---

- 랜덤 모듈을 사용하기 위해서는 `import random` 필요
    - random.random() : 0.0~1.0 미만의 실수값 반환
    - random.randint(1, 10) : 1~10 사이의 정수 반환
    - random.randrange(0, 10, 2) : 0~10 미만의 2의 배수만 반환
    - random.choice() : 자료형 변수에서 임의의 값 반환
    - random.sample() : 자료형 변수에서 필요한 개수만큼 반환
    - random.shuffle() : 자료형 변수 내용을 랜덤으로 셔플