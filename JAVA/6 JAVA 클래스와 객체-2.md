# 6. JAVA 클래스와 객체-2

Author: jk s
Category: JAVA
Created Time: 2022년 11월 24일 오후 2:55
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 24일 오후 4:08

## 생성자

---

**생성자 개념**

- 객체가 생성될 때 초기화를 위해 실행되는 메소드

**생성자의 특징**

- 생성자는 메소드
- 생성자 이름은 클래스 이름과 반드시 동일
- 생성자 여러개 작성 가능(오버로딩)
- 생성자는 new를 통해 객체를 생성할 때, 객체당 한 번 호출
- 생성자는 리턴 타입을 지정할 수 없음
- 생성자의 목적은 객체 초기화
- 생성자는 객체가 생성될 때 반드시 호출됨

```java
// 생성자 선언 및 활용 예제
public class Book {
	String title;
	String author;
	
	public Book(String t) { // 생성자
		title = t; author = "작자미상";
	}
	
	public Book(String t, String a) { // 생성자
		title = t; author = a;
	}
	
	public static void main(String [] args) {
		Book littlePrince = new Book("어린왕자", "생텍쥐페리"); 
		Book loveStory = new Book("춘향전"); 
		System.out.println(littlePrince.title + " " + littlePrince.author);
		System.out.println(loveStory.title + " " + loveStory.author);
	}
}
/* 실행 결과
어린왕자 생텍쥐페리
춘향전 작자미상
*/
```

## 기본 생성자

---

**기본 생성자**

- 매개 변수 없고 아무 작업 없이 단순 리턴하는 생성자
- 디폴트 생성자라고도 부름
- 클래스에 생성자가 하나도 선언되지 않은 경우, 컴파일러에 의해 자동으로 삽입된다.

## this 레퍼런스

---

- 객체 자신에 대한 레퍼런스
- 컴파일러에 의해 자동 관리, 개발자는 사용하기만 하면 됨
- `this.멤버` 형태로 멤버 사용

**this의 필요성**

- 객체의 멤버 변수와 메소드 변수의 이름이 같은 경우
- 다른 메소드 호출 시 객체 자신의 레퍼런스를 전달 할 때
- 메소드가 객체 자신의 레퍼런스를 반환 할 때

**객체 속에서의 this**

![Untitled](https://user-images.githubusercontent.com/114375741/203719106-e5fe4864-2998-4c1b-900b-912755d796c4.png)


**`this()`로 다른 생성자 호출**

- 클래스 내의 다른 생성자 호출
- 생성자 내에서만 사용 가능
- 반드시 생성자 코드의 제일 처음에 수행

```java
// this()로 다른 생성자 호출 예제
public class Book {
	String title;
	String author;
	void show() { System.out.println(title + " " + author); }

	public Book() {
		this("", "");
		System.out.println("생성자 호출됨");
	}

	public Book(String title) {
		this(title, "작자미상");
	}

	public Book(String title, String author) {
		this.title = title; this.author = author;
	}
	public static void main(String [] args) {
		Book littlePrince = new Book("어린왕자", "생텍쥐페리");
		Book loveStory = new Book("춘향전");
		Book emptyBook = new Book();		
		loveStory.show();
	}
}
/* 실행 결과
생성자 호출됨
춘향전 작자미상
*/
```

## 메소드 형식

---

**메소드**

- 클래스의 멤버 함수
- 자바의 모든 메소드는 반드시 클래스 안에 있어야 함(캡슐화)

**메소드 구성 형식**

- 접근 지정자
- 리턴 타입(메소드가 반환하는 값의 데이터 타입)

![Untitled 1](https://user-images.githubusercontent.com/114375741/203719086-b722afb2-cec6-4ea0-9181-504c762b9582.png)

## 메소드 오버로딩(Overloading)

---

- 이름이 같은 메소드 작성**(**매개변수의 개수나 타입이 서로 다르고 이름이 동일한 메소드들)
- 리턴 타입은 오버로딩과 관련 없음

**오버로딩 된 메소드 호출**

![Untitled 2](https://user-images.githubusercontent.com/114375741/203719093-a81c22ab-637b-4403-8b23-c2eda1bec490.png)

## 패키지

---

- 관련 있는 클래스 파일(컴파일된.class)을 저장하는 디렉터리
- 자바 응용프로그램은 하나 이상의 패키지로 구성
![Untitled 3](https://user-images.githubusercontent.com/114375741/203719097-d47d61de-3fa7-47ca-ab11-6a40d9438041.png)

## 접근 지정자

---

**자바의 접근 지정자 4가지**

- private, protected, public, default(접근지정자 생략)

**접근 지정자의 목적**

- 클래스나 일부 멤버를 공개하여 다른 클래스에서 접근하도록 허용
- 접근 지정은 캡슐화에 묶인 보호를 일부 해제할 목적

**접근 지정자에 따른 클래스나 멤버의 공개 범위**

![Untitled 4](https://user-images.githubusercontent.com/114375741/203719102-baf43b6f-922f-4435-a25a-64b6f807f87c.png)
![Untitled 5](https://user-images.githubusercontent.com/114375741/203719103-dcec653a-d2ee-447d-99ef-2286578d38b1.png)

## final 클래스와 메소드

---

- final 클래스 : 클래스 상속 불가
- final 메소드 : 오버라이딩 불가

**final 필드, 상수 선언**

- 상수를 선언할 때 사용
- 상수 필드는 선언 시에 초기 값을 지정하여야 한다.
- 상수 필드는 실행 중에 값을 변경할 수 없다.
