# 9. Python 객체와 클래스

Author: jk s
Category: Python
Created Time: 2022년 11월 18일 오후 12:03
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 18일 오후 12:46

## 객체(Object)

---

- 객체란 존재하는 모든 것들을 의미
- 객체는 속성과 기능을 가지고 있는 것이 핵심

## 클래스(Class)

---

- 객체의 구성 요소를 담는 개념
- 여러개의 속성(Attribute)과 메소드(Method)를 포함하는 개념
- 인스턴스는 메모리에 할당된 객체를 의미

```python
# 클래스 문법
class Name(object):
# class : 클래스 정의
# Name : 클래스 명
# object : 상속받는 객체 명
```

### (예제) 클래스 정의

---

- 클래스 이름: Book
- 속성
    - 저자: author
    - 책 이름: name
    - 출판사: publisher
    - 발행일: date

```python
class Book(object):
  author = ""
  title = ""
  publisher = ""
  date = ""

book = Book()
book.author = "jjsin123"
print(book.author)
book.title = "Python Programming"
print(book.title)

'''
jjsin123
Python Programming
'''
```

### (예제) **클래스 메소드 정의**

---

**메소드**

- 책 정보 출력: `print_info(self)`
- `self`가 있어야만 실제로 인스턴스가 사용할 수 있는 메소드로 선언
- `print_info(self)`에서 `self`는 실제적으로 `book` 인스턴스를 의미
- 메소드 안에서 속성 값을 사용하지 않을 경우에는 `self` 생략 가능

```python
class Book(object):
  author = ""
  title = ""
  publisher = ""
  date = ""
  def print_info(self):   # self -> 자바의 this와 비슷
    print("Author:", self.author)
    print("Title:", self.title)

book = Book()
book.author = "jjsin123"
book.title = "Python Programming"
book.print_info()

'''
Author: jjsin123
Title: Python Programming
'''
```

### (예제) **인스턴스 속성**

---

- 인스턴스 속성은 객체로부터 인스턴스가 생성된 후에 인스턴스에서 활용하는 속성
- `Book` 클래스에서 생성된 인스턴스 `b1`에서 속성을 활용

```python
class Book(object):
  author = ""
  title = ""
  publisher = ""
  date = ""
  def print_info(self):
    print("Author:", self.author)
    print("Title:", self.title)
    print("Publisher:", self.publisher)
    print("Date:", self.date)

b1 = Book() # 인스턴스
b1.author = "jjsin123"
b1.title = "Python Programming"
b1.publisher = "Colab"
b1.date = "2022"
b1.print_info()

'''
Author: jjsin123
Title: Python Programming
Publisher: Colab
Date: 2022
'''
```

### (예제) 클래스 속성

---

- 클래스 속성은 클래스 자체에서 사용되는 속성

```python
class Book(object):
  author = ""
  title = ""
  publisher = ""
  date = ""
  def print_info(self):
    print("Author:", self.author)
    print("Title:", self.title)
    print("Publisher:", self.publisher)
    print("Date:", self.date)

b1 = Book()
Book.author = "jjsin123"      # b1.author = "jjsin123" : O      Book.author : X  목적에 맞게 사용할것
Book.title = "Python Programming"
Book.publisher = "Colab"
Book.date = "2020"
b1.print_info()

'''
Author: jjsin123
Title: Python Programming
Publisher: Colab
Date: 2020
'''
```

### (예제) 인스턴스 속성과 클래스 속성의 활용

---

**인스턴스 속성과 클래스 속성을 목적에 맞도록 나누어서 활용**

- 인스턴스 속성
    - 저자: author
    - 제목: title
    - 출판사: publisher
    - 발행일: date
- 클래스 속성
    - 수량: count

```python
class Book(object):
  author = ""
  title = ""
  publisher = ""
  date = ""
  count = 0
  def print_info(self):
    print("Author:", self.author)
    print("Title:", self.title)
    print("Publisher:", self.publisher)
    print("Date:", self.date)

b1 = Book()
Book.count += 1 # 클래스 속성
b1.author = "jjsin123" # 여기부터 아래는 인스턴스 속성
b1.title = "Python Programming"
b1.publisher = "Colab"
b1.date = "2020"
b1.print_info()
print("Number of Books:", str(Book.count))

'''
Author: jjsin123
Title: Python Programming
Publisher: Colab
Date: 2020
Number of Books: 1
'''
```

## 클래스 매직 메소드

---
![Untitled](https://user-images.githubusercontent.com/114375741/202612771-afb1c6f6-3a21-451c-911d-9cd7ee4b39b9.png)

## 클래스 상속

---

- 기존 클래스에 있는 속성과 메소드를 그대로 상속받아 새로운 클래스를 생성
- 공통된 클래스를 부모로 두고 자식들이 상속을 받아 클래스를 생성하므로 일관성있는 프로 그래밍 가능
- 기존 클래스에서 일부를 추가/변경한 새로운 클래스 생성으로 코드 재사용(reuse) 가능
- 클래스 상속 문법: class SubClass(SuperClass):

```python
class SuperClass(object):
  pass
class SubClass(SuperClass):
  pass
```

### 메소드 오버라이딩

---

- SuperClass 로부터 SubClass1 와 SubClass2 가 클래스 상속
- 아무 내용도 없는 추상 메소드(Abstract Method) method() 를 정의
- SubClass1 의 method() 는 SuperClass 의 추상 메소드를 오버라이딩

```python
class SuperClass(object):
  def method(self):
    pass
class SubClass1(SuperClass):
  def method(self):
    print("Method Overriding")
class SubClass2(SuperClass):
  pass

sub1 = SubClass1()
sub2 = SubClass2()
sub1.method()
sub2.method()
'''
Method Overriding
'''
```

### 클래스 상속, 메소드 오버라이딩 예제

---

- Vehicle 클래스를 상속받아 Car 클래스와 Truck 클래스 생성
- Car 클래스와 Truck 클래스는 up_speed 메소드를 오버라이딩
- Car 클래스는 속도가 240 초과되면 240으로 조정
- Truck 클래스는 속도가 180 초과되면 180으로 조정

```python
class Vehicle(object):
  speed = 0
  def up_speed(self, value):
    self.speed += value
  
  def down_speed(self, value):
    self.speed -= value
  
  def print_speed(self):
    print("Speed:", str(self.speed))
class Car(Vehicle):
  def up_speed(self, value):
    self.speed += value
    if self.speed > 240: self.speed = 240
class Truck(Vehicle):
  def up_speed(self, value):
    self.speed += value
    if self.speed > 180: self.speed = 180
```

```python
car = Car()
car.up_speed(300)
car.print_speed()
truck = Truck()
truck.up_speed(200)
truck.print_speed()
'''
**********Speed: 240
Speed: 180
'''**********
```
