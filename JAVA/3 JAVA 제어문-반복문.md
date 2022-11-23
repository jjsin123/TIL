# 3. JAVA 제어문-반복문

Author: jk s
Category: JAVA
Created Time: 2022년 11월 23일 오전 11:14
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 23일 오전 11:33

## 자바 반복문의 종류

---

- for문
- while문
- do while문

## for문의 구성

---

![Untitled](https://user-images.githubusercontent.com/114375741/203459544-f6904304-3d58-44b1-97a2-87cc75cc6ba4.png)

## for문의 실행과정 순서도

---

![Untitled 1](https://user-images.githubusercontent.com/114375741/203459530-5f45ae6f-82d7-4fff-8f75-bb0e149e6186.png)

```java
// for문 예제
// 1부터 10까지 합 출력
public class ForSample {
	public static void main(String[] args) {
		int sum=0;
		
		for(int i=1; i<=10; i++) { // 1~10까지 반복
			sum += i;
			System.out.print(i); // 더하는 수 출력

			if(i<=9) // 1~9까지는 '+' 출력
				System.out.print("+");
			else { // i가 10인 경우 
				System.out.print("="); // '=' 출력하고
				System.out.print(sum); // 덧셈 결과 출력
			}
		}
	}
}
// 실행 결과
// 1+2+3+4+5+6+7+8+9+10=55
```

## while문의 구성

---

- 반복 조건이 true이면 반복, false이면 반복 종료
- 반복 조건이 없으면 컴파일 오류
- 처음부터 반복조건을 통과한 후 작업문 수행

![Untitled 2](https://user-images.githubusercontent.com/114375741/203459536-335cef20-2451-48cd-a4d7-087d1f3715dc.png)

## while문 실행 과정 순서도

---

![Untitled 3](https://user-images.githubusercontent.com/114375741/203459540-994c2418-3837-4b6d-abc5-366a2bd5bbd4.png)

```java
// while문 예제
// 정수를 여러 개 입력 받고 평균을 출력하라. -1이 입력되면 입력을 종료
import java.util.Scanner;
public class WhileSample {
	public static void main(String[] args) {
		int count=0; // count는 입력된 정수의 개수
		int sum=0; // sum은 합
		Scanner scanner = new Scanner(System.in);		
		System.out.println("정수를 입력하고 마지막에 -1을 입력하세요.");

		int n = scanner.nextInt(); // 정수 입력
		while(n != -1) { // -1이 입력되면 while 문 벗어남
			sum += n;
			count++;
			n = scanner.nextInt(); // 정수 입력
		}
		if(count == 0) System.out.println("입력된 수가 없습니다.");
		else {
			System.out.print("정수의 개수는 " + count + "개이며 ");
			System.out.println("평균은 " + (double)sum/count + "입니다.");
		}
		scanner.close();
	}
}
/* 실행 결과
정수를 입력하고 마지막에 -1을 입력하세요.
10 30 –20 40 -1
정수의 개수는 4개이며 평균은 15.0입니다.
*/
```

## 중첩 반복

---

- 반복문이 다른 반복문을 내포하는 구조
- 이론적으로는 몇 번이고 중첩 반복 가능
- 너무 많은 중첩 반복은 프로그램 구조를 복잡하게 하므로 2중 또는 3중 반복이 적당하다.

```java
// 중첩 반복문 예제
// 2중첩 for문을 사용하여 구구단을 출력하시오
public class NestedLoop {
	public static void main(String[] args) {
		for(int i=1; i<10; i++) { // 1단에서 9단
			for(int j=1; j<10; j++) { // 각 단의 구구셈 출력
				System.out.print(i + "*" + j + "=" + i*j); // 구구셈 출력
				System.out.print('\t'); // 하나씩 탭으로 띄기
			}
			System.out.println(); // 한 단이 끝나면 다음 줄로 커서 이동
		}
	}
}
/* 실행 결과
1*1=1	1*2=2	1*3=3	1*4=4	1*5=5	1*6=6	1*7=7	1*8=8	1*9=9
2*1=2	2*2=4	2*3=6	2*4=8	2*5=10	2*6=12	2*7=14	2*8=16	2*9=18
3*1=3	3*2=6	3*3=9	3*4=12	3*5=15	3*6=18	3*7=21	3*8=24	3*9=27
4*1=4	4*2=8	4*3=12	4*4=16	4*5=20	4*6=24	4*7=28	4*8=32	4*9=36
5*1=5	5*2=10	5*3=15	5*4=20	5*5=25	5*6=30	5*7=35	5*8=40	5*9=45
6*1=6	6*2=12	6*3=18	6*4=24	6*5=30	6*6=36	6*7=42	6*8=48	6*9=54
7*1=7	7*2=14	7*3=21	7*4=28	7*5=35	7*6=42	7*7=49	7*8=56	7*9=63
8*1=8	8*2=16	8*3=24	8*4=32	8*5=40	8*6=48	8*7=56	8*8=64	8*9=72
9*1=9	9*2=18	9*3=27	9*4=36	9*5=45	9*6=54	9*7=63	9*8=72	9*9=81
*/
```

## continue문

---

- 반복문을 빠져 나가지 않으면서 다음 반복으로 진행

![Untitled 4](https://user-images.githubusercontent.com/114375741/203459542-3bd89cf7-b51a-42c1-a1b0-db83c5922b9e.png)

```java
// continue문 예제
// 5개의 정수를 입력 받고 그 중 양수들만 합하는 프로그램을 작성하라
import java.util.Scanner;

public class ContinueExample {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("정수를 5개 입력하세요.");
		int sum=0;
		for(int i=0; i<5; i++) {
			int n = scanner.nextInt(); // 키보드에서 정수 입력
			if(n<=0) 
				continue; // 양수가 아닌 경우 다음 반복으로 진행
			else 
				sum += n; // 양수인 경우 덧셈
		}
		System.out.println("양수의 합은 " + sum);
		
		scanner.close();
	}
}
/*
정수를 5개 입력하세요.
5
-2
6
10
-4
양수의 합은 21
*/
```

## break문

---

- 반복문을 완전히 빠져 나갈 때 사용
- 하나의 반복문만 벗어남
- 중첩 반복의 경우 안쪽 반복문의 break문이 실행되면 안쪽 반복문만 벗어남

![Untitled 5](https://user-images.githubusercontent.com/114375741/203459543-f34f7396-ba3c-484d-aacb-b23ed718c6c0.png)

```java
// break예제
// exit가 입력되면 while문을 벗어나도록 break문을 활용하라
import java.util.Scanner;

public class BreakExample {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.println("exit을 입력하면 종료합니다.");
		while(true) {
			System.out.print(">>");
			String text = scanner.nextLine();
			if(text.equals("exit")) // "exit"이 입력되면 반복 종료
				break; // while 문을 벗어남
		}
		System.out.println("종료합니다...");
 
		scanner.close();
	}
}
/*
exit을 입력하면 종료합니다.
>>edit
>>exit
종료합니다...
*/
```
