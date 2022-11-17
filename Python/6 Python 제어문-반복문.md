# 6. Python 제어문-반복문

Author: jk s
Category: Python
Created Time: 2022년 11월 17일 오후 12:23
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 17일 오후 1:30

## 반복문

---

- 문장을 반복적으로 수행하는 문장으로 정해진 동작을 반복하여 처리할 때 사용
- 파이썬에서 제공하는 반복문 : `while` , `for`

### while 문

---

- 어떤 조건이 만족하는 동안 문장을 수행하고 만족하지 않는 경우 수행 중단

```python
# while 문 기본 문법
while <조건>:
 <문장>
```

```python
# while 문 예제 : 1부터 10까지 반복
i = 1
while i <= 10:
	print(i)
	i += 1
'''
1
2
3
4
5
6
7
8
9
10
'''
# while 문 예제2: 1부터 10까지 더하기
i = 1
sum = 0
while i <= 10:
	sum += i
	i += 1
print(sum)
'''
55
'''
# while 문 예제3: 리스트에서 요소 끄집어 내기
vip_list=['Kim','Lee','Park']
while vip_list:
	print(vip_list.pop(0)) # pop은 인덱스의 요소를 꺼내고 삭제한다
	print('Remaining : {}'.format(len(vip_list))) # list 내 남아있는 요소개수 출력
'''
Kim
Remaining : 2
Lee
Remaining : 1
Park
Remaining : 0
'''
```

### for문

---

- 반복 범위를 지정하여 반복 수행

```python
# for문 기본 문법
for VARIABLE in ITERABLE_OBJECT:
 STATEMENT
```

```python
# for문 예제
for i in range(2):
	print('Inside for loop')
	print('Outside for loop')
'''
Inside for loop
Outside for loop
Inside for loop
Outside for loop
'''
# 예제2
for i in range(1,3,1): # (시작,마지막 앞,몇개씩)
	print('i='+str(i))
'''
i=1
i=2
'''
# 리스트 요소 반복 예제
list = ['One', 'Two', 'Three']
for i in list:
	print(i)
'''
One
Two
Three
'''
# 리스트 요소 반복 예제2
for i in [1,2,3,4,5]:
	print('i='+str(i))
'''
i=1
i=2
i=3
i=4
i=5
'''
# 튜플 요소 반복 예제
tuple = ('One', 'Two', 'Three')
for i in tuple:
	print(i)
'''
One
Two
Three
'''
# 문자열 요소 반복 예제
string = "Python"
for i in string:
	print(i)
'''
P
y
t
h
o
n
'''
# 문자열 요소 반복 예제2
for i in 'abcde':
	print('i='+i)
'''
i=a
i=b
i=c
i=d
i=e
'''
# dictionary 요소 반복 예제
D={'P1':20,'P2':30,'P3':40}
for i in D.items(): # D.keys() D.values()
	print('i='+str(i))
'''
i=('P1', 20)
i=('P2', 30)
i=('P3', 40)
'''
# 중첩 for 예제
for i in [1,2,3]:
	for j in [1,2,3]:
		print('{}*{}={}'.format(i,j,i*j))
'''
1*1=1
1*2=2
1*3=3
2*1=2
2*2=4
2*3=6
3*1=3
3*2=6
3*3=9
'''
# 중첩 for 예제2
for i in [1,2]:
	for j in [1,2]:
		print('i='+str(i))
		print('j='+str(j))
'''
i=1
j=1
i=1
j=2
i=2
j=1
i=2
j=2
'''
# 중첩 for 예제3
for i in range(2,3,1):
  for j in range(1,10,1):
    print('{}*{}={}'.format(i,j,i*j))
'''
2*1=2
2*2=4
2*3=6
2*4=8
2*5=10
2*6=12
2*7=14
2*8=16
2*9=18
'''
```

### else 문

---

- 반복이 종료된 후에 한번 더 실행되는 문장

```python
# while-else문 예제
i = 1
sum = 0
while i <= 10:
	sum += i
	i += 1
else:
	print(sum)
'''
55
'''
# for-else문 예제
sum = 0
for i in range(11):
	sum += i
else:
	print(sum)
'''
55
'''
```

### break 문

---

- 반복문 종료

```python
# break 예제
i = 0
while i < 100:
	print(i)
	if i == 2:
		break
	i += 1
'''
0
1
2
'''
# break 예제2
for i in range(100):
	print(i)
	if i == 2:
		break
'''
0
1
2
'''
```

### continue 문

---

- 반복 조건문으로 이동

```python
# contunue 예제
temp = [18,-5,20,50,-17,9]
while temp:
	t=temp.pop(0)
	if t < 0:
		continue
	print(t)
'''
18
20
50
9
'''
# contunue 예제2
temp = [18,-5,20,50,-17,9]
for i in temp:
	if i < 0 :
		continue
	print('Temp = {}'.format(i))
'''
Temp = 18
Temp = 20
Temp = 50
Temp = 9
'''
```

### 리스트 내포

---

- 리스트 안에 for문과 if문 사용

```python
# 예제1
list = [1, 2, 3, 4, 5]
print([i * 2 for i in list])
print([i * 2 for i in range(10) if i % 2 == 0])
'''
[2, 4, 6, 8, 10]
[0, 4, 8, 12, 16]
'''
# 예제2
num_list = [x for x in range(20) if x%2==0]
print(num_list)
'''
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
'''
```