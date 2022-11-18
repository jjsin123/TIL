# 7. Python 입력과 출력

Author: jk s
Category: Python
Created Time: 2022년 11월 18일 오전 9:05
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 18일 오전 10:04

## 표준 입출력

---

### 표준 입력 함수

---

- `input()` : 콘솔 창을 통해서 사용자 입력을 받는 표준 입력 함수
- 함수 안에 입력 받기 위한 질문을 텍스트로 넣을 수 있음

```python
# input() 예제1
name = input("이름: ")
print(name)

''' 실행 결과
이름: centum
centum
'''

# 예제2 구구단 중의 하나의 단을 입력받아 계산
i = int(input("출력할 단: "))
for j in range(1, 10):
	print("{0} x {1} = {2}".format(i, j, i * j))

''' 실행 결과
출력할 단: 4
4 x 1 = 4
4 x 2 = 8
4 x 3 = 12
4 x 4 = 16
4 x 5 = 20
4 x 6 = 24
4 x 7 = 28
4 x 8 = 32
4 x 9 = 36
'''
```

### 표준 출력 함수

---

- `print()` : 콘솔 창을 통해서 결과를 출력하는 표준 출력 함수
- `sep=’separator’` : 개체가 분리하는 방법 지정, 기본값은 ’ ‘
- `end=’end’` : 끝에 출력할 항목 지정, 기본값은 ‘\n’
- `file` : 쓰기 방법이 있는 객체, 기본값은 sys.stdout
- `flush` : True일 경우 flush하고, False일 경우 버퍼, 기본값은 False

```python
print("Hello", "Python", sep = "---")
print(1, 2, 3)
print(1, end=' ')
'''
[1, 2, 3]
Hello---Python
1 2 3
'''
```

## 파일 입출력

---

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled.png)

### 파일 입출력 과정

---

- 파일의 입출력 과정은 단계를 가짐
- 파일을 열고, 파일을 읽거나 쓰고, 파일을 닫는 순서

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled%201.png)

### 파일 열기/닫기

---

- file.txt 파일을 생성하고, 열고 닫기

```python
# 기본 형식
f = open("file.txt", 'w')
f = open("file.txt", 'r')
f.close()
```

### 파일 모드

---

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled%202.png)

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled%203.png)

### 텍스트 파일 쓰기

---

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled%204.png)

- `write()`를 이용하여 파일에 쓰기

```python
f = open("file.txt", 'w')
f.write("Hello Python")
f.close()
!cat file.txt
# Hello Python
```

- `writelines()`를 이용하여 list를 파일에 쓰기

```python
list = ["One\n", "Two\n", "Three\n"]
f = open("file.txt", 'w')
f.writelines(list)
f.close()
!cat file.txt
'''
One
Two
Three
'''
```

**표준입력 → 파일쓰기**

- 표준 입력을 `input()` 함수를 통해 입력 받고, `write()` 함수를 통해 파일에 쓰기

```python
text = input("입력: ")
f = open("file.txt", 'w')
f.write(text)
f.close()
# 입력: jjsin123
!cat file.txt
# jjsin123
```

### 텍스트 파일 출력

---

![Untitled](7%20Python%20%E1%84%8B%E1%85%B5%E1%86%B8%E1%84%85%E1%85%A7%E1%86%A8%E1%84%80%E1%85%AA%20%E1%84%8E%E1%85%AE%E1%86%AF%E1%84%85%E1%85%A7%E1%86%A8%205bbab37de957427cb930da7b73063e6d/Untitled%205.png)

```python
# 텍스트 파일 예제
!echo "동해물과 백두산이 마르고 닳도록" > anthem.txt
!echo "하느님이 보우하사 우리나라 만세" >> anthem.txt
```

- `readline()`를 이용하여 텍스트 파일을 라인 단위로 읽고 화면에 출력

```python
f = open("anthem.txt", 'r')
lines = f.readlines()
print(lines)
f.close()
# ['동해물과 백두산이 마르고 닳도록\n', '하느님이 보우하사 우리나라 만세\n']
```

- `read()`를 이용하여 텍스트 파일을 읽고 화면에 출력

```python
f = open("anthem.txt", 'r')
data = f.read()
print(data)
f.close()
'''
동해물과 백두산이 마르고 닳도록
하느님이 보우하사 우리나라 만세
'''
```

**with문**

- 항상 파일을 `open()` 함수로 열고, `close()` 함수로 닫아야 하는 일을 자동으로 처리
- with문을 이용하면 with 블록 내에서 파일을 열고 벗어나면 파일을 닫음

```python
f = open("file.txt", 'w')
f.write("Hello Python")
f.close()
```

```python
with open("file.txt", 'w') as f:
  f.write("Hello Python")
```