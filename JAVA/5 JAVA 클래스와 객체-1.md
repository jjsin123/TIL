# 5. JAVA 클래스와 객체-1

Author: jk s
Category: JAVA
Created Time: 2022년 11월 24일 오후 1:38
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 24일 오후 2:57

## 캡슐화

---

- 객체를 캡슐로 싸서 내부를 볼 수 없게 하는 것
- 외부의 접근으로부터 객체 보호

**클래스(class)** : 객체 모양을 선언한 틀(캡슐화)

- 메소드(멤버 함수)와 필드(멤버 변수)는 모두 클래스 내에 구현

**객체**

- 클래스의 모양대로 생성된 실체(instance)
- 객체 내 데이터에 대한 보호, 외부 접근 제한

## 상속

---

**상속**

- 상위 개체의 속성이 하위 개체에 물려짐
- 하위 개체가 상위 개체의 속성을 모두 가진다

**자바의 상속**

- 자식 클래스가 부모 클래스의 속성을 물려받고, 기능을 확장
- 부모 클래스 : 수퍼 클래스
- 하위 클래스 : 서브 클래스, 수퍼 클래스를 잿용하고 새로운 특성 추가
- 자바는 클래스 다중 상속 없음!! 인터페이스 다중 상속은 허용!!

![Untitled](5%20JAVA%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A2%E1%84%89%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6-1%20ee004f3c227240f69f49b5a4733d8a16/Untitled.png)

## 다형성

---

- 같은 이름의 메소드가 클래스나 객체에 따라 다르게 동작하도록 구현

**다형성 사례**

- 메소드 오버로딩 : 같은 이름이지만 다르게 작동하는 여러 메소드
- 메소드 오버라이딩 : 슈퍼클래스의 메소드를 서브 클래스마다 다르게 구현

## 클래스 구성

---

**클래스 선언**

- class 키워드로 선언
- 클래스는 {로 시작하여 }로 닫으며 이곳에 모든 필드와 메소드 구현
- 클래스 접근 권한(default,public,protected,private)

**필드와 메소드**

- 필드(field) : 객체 내에 값을 저장하는 멤버 변수
- 메소드(method) : 함수이며 객체의 행동(행위)를 구현

**필드의 접근 지정자**

- 필드나 메소드 앞에 붙어 다른 클래스의 접근 허용을 표시

**생성자**

- 클래스의 이름과 동일한 특별한 메소드
- 객체가 생성될 때 자동으로 한 번 호출되는 메소드

![Untitled](5%20JAVA%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A2%E1%84%89%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6-1%20ee004f3c227240f69f49b5a4733d8a16/Untitled%201.png)

## 객체 생성 및 접근

---

**객체 생성**

- 반드시 new 키워드를 이용해서 생성

**객체 생성 과정**

- 객체에 대한 레퍼런스 변수 선언

**객체의 멤버 접근**

- 객체 레퍼런스 멤버

![Untitled](5%20JAVA%20%E1%84%8F%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A2%E1%84%89%E1%85%B3%E1%84%8B%E1%85%AA%20%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6-1%20ee004f3c227240f69f49b5a4733d8a16/Untitled%202.png)

```java
// Circle 클래스의 객체 생성 및 활용 예제
public class Circle {
	int radius; 					// 원의 반지름 필드
	String name; 				// 원의 이름 필드

	public Circle() { }			// 원의 생성자

	public double getArea() { 	// 원의 면적 계산 메소드
		return 3.14*radius*radius;
	}

	public static void main(String[] args) {
		Circle pizza; 
		pizza = new Circle(); 					// Circle 객체 생성
		pizza.radius = 10; 						// 피자의 반지름을 10으로 설정
		pizza.name = "자바피자"; 			// 피자의 이름 설정
		double area = pizza.getArea(); 		// 피자의 면적 알아내기
		System.out.println(pizza.name + "의 면적은 " + area);

		Circle donut = new Circle(); 		// Circle 객체 생성
		donut.radius = 2; 						// 도넛의 반지름을 2로 설정
		donut.name = "자바도넛"; 			// 도넛의 이름 설정
		area = donut.getArea(); 				// 도넛의 면적 알아내기
		System.out.println(donut.name + "의 면적은 " + area);
	}
}
/* 실행 결과
자바피자의 면적은 314.0
자바도넛의 면적은 12.56
*/
```