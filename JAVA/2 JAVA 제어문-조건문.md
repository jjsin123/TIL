# 2. JAVA 제어문-조건문

Author: jk s
Category: JAVA
Created Time: 2022년 11월 23일 오전 11:01
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 23일 오전 11:17

## 단순 if문

---

if의 괄호 안에 조건식(논리형 변수나 논리 연산)

- 실행문장이 단일 문장인 경우 둘러싸는 {, } 생략 가능

![Untitled](2%20JAVA%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20948582a8ea5e48239af26a36e685baef/Untitled.png)

```java
// if문 사용하기 예제

import java.util.Scanner;

public class SuccessOrFail {
	public static void main (String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.print("점수를 입력하시오: ");
		int score = scanner.nextInt();
		if (score >= 80)
			System.out.println("축하합니다! 합격입니다.");
		
		scanner.close();
	}
}
/* 실행 결과
점수를 입력하시오: 95
축하합니다! 합격입니다.
*/
```

## if-else 문

---

- 조건식이 true면 실행문장1 실행 후 if-else문을 벗어남
- flase인 경우에 실행문장2 실행 후, if-else문을 벗어남

![Untitled](2%20JAVA%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20948582a8ea5e48239af26a36e685baef/Untitled%201.png)

```java
// if-else 예제
// 입력된 수가 3의 배수인지 판별하는 프로그램을 작성하시오
import java.util.Scanner;

public class MultipleOfThree {
	public static void main (String[] args) {
		Scanner scanner = new Scanner(System.in);

		System.out.print("수를 입력하시오: ");
		int number = scanner.nextInt();

		if (number % 3 == 0)
			System.out.println("3의 배수입니다.");
		else 
			System.out.println("3의 배수가 아닙니다.");

		scanner.close();
	}
}
/* 실행 결과
수를 입력하시오: 129
3의 배수입니다.
*/
```

## 다중 if-else문

---

- if-else가 연속되는 모양
- 조건문이 너무 많은 경우, switch 문 사용 권장

![Untitled](2%20JAVA%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20948582a8ea5e48239af26a36e685baef/Untitled%202.png)

```java
// 중첩 if-else문 예제
// 점수와 학년을 입력 받아 60점 이상이면 합격, 미만이면 불합격을 출력한다.
// 4학년의 경우 70점 이상이어야 합격이다.
import java.util.Scanner;
public class NestedIf {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);

		System.out.print("점수를 입력하세요(0~100): ");
		int score = scanner.nextInt(); 

		System.out.print("학년을 입력하세요(1~4): ");
		int year = scanner.nextInt(); 

		if(score >= 60) { // 60점 이상
			if(year != 4)
				System.out.println("합격!"); // 4학년 아니면 합격
			else if(score >= 70)
				System.out.println("합격!"); // 4학년이 70점 이상이면 합격
			else
				System.out.println("불합격!"); // 4학년이 70점 미만이면 불합격
		}
		else // 60점 미만 불합격
			System.out.println("불합격!");

		scanner.close();
	}
}
/*실행 결과
점수를 입력하세요(0~100): 65
학년을 입력하세요(1~4): 4
불합격!
*/
```

## switch 문

---

- switch문은 식과 case문의 값과 비교
- case의 비교 값과 일치하면 해당 case의 실행문장 수행
- break를 만나면 switch문을 벗어남
- case의 비교 값과 일치하는 것이 없으면 default문 실행
- default문은 생략 가능

![Untitled](2%20JAVA%20%E1%84%8C%E1%85%A6%E1%84%8B%E1%85%A5%E1%84%86%E1%85%AE%E1%86%AB-%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%E1%84%86%E1%85%AE%E1%86%AB%20948582a8ea5e48239af26a36e685baef/Untitled%203.png)

```java
// switch문 예제
// switch문을 이용하여 커피 메뉴의 가격을 알려주는 프로그램을 작성하라.
import java.util.Scanner;
public class CoffeePrice {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.print("무슨 커피 드릴까요? ");
		String order = scanner.next();
		int price=0;
		switch (order) {
			case "에스프레소":
			case "카푸치노":
			case "카페라떼":
				price = 3500;
				break;
			case "아메리카노" :
				price = 2000;
				break;
			default:
				System.out.println("메뉴에 없습니다!");
		}
		if(price != 0)
			System.out.print(order + "는 " + price + "원입니다");
		scanner.close();
	}
}
/* 실행 결과
무슨 커피 드릴까요? 에스프레소
에스프레소는 3500원입니다
*/
```