# 4. JAVA 배열

Author: jk s
Category: JAVA
Created Time: 2022년 11월 23일 오후 12:10
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 23일 오후 2:19

## 배열(array)이란?

---

- 인덱스와 인덱스에 대응하는 데이터들로 이루어진 자료 구조
- 배열을 이용하면 한 번에 많은 메모리 공간 할당 가능
- 같은 타입의 데이터들이 순차적으로 저장
- 인덱스를 이용하여 원소 데이터 접근
- 반복문을 이용하여 처리하기에 적합
- 배열 인덱스
- 0부터 시작
- 인덱스는 배열의 시작 위치에서부터 데이터가 있는 상대 위치

## 일차원 배열 만들기

---

- 배열의 선언과 배열의 생성 두 단계 필요
- 배열 선언

int intArray[]; 또는 int [] intArray;

char charArray[]; 또는 char []charArray;

- 배열 생성

intArray = new int[10]; 또는 int intArray[] = new int[10];

charArray = new char[20]; 또는 char charArray[] = new char[20];

## 래퍼런스 변수와 배열

---

![Untitled](4%20JAVA%20%E1%84%87%E1%85%A2%E1%84%8B%E1%85%A7%E1%86%AF%208a3e7169b6054bee8ac5c6199be5637e/Untitled.png)

## 배열 인덱스와 원소 접근

---

- 배열 원소 접근
- 배열 변수명과 [] 사이에 원소의 인덱스를 적어 접근
- 배열의 인덱스는 0부터 시작
- 배열의 마지막 항목의 인덱스는 (배열 크기-1)

```java
// 배열 예제
// 양수 5개를 입력 받아 배열에 저장하고 제일 큰 수를 찾아보자
import java.util.Scanner;

public class ArrayAccess {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
 
		int intArray[] = new int[5]; // 배열 생성

		int max=0; 		// 현재 가장 큰 수
		System.out.println("양수 5개를 입력하세요.");		
		for(int i=0; i<5; i++) {
			intArray[i] = scanner.nextInt(); // 입력받은 정수를 배열에 저장
			if(intArray[i] >max) // intArray[i]가 현재 가장 큰 수보다 크면
				max = intArray[i]; // intArray[i]를 max로 변경
		}
		System.out.print("가장 큰 수는 " + max + "입니다.");
		
		scanner.close();
	}
}
/* 실행 결과
양수 5개를 입력하세요.
1
39
78
100
99
가장 큰 수는 100입니다.
*/
```

## 배열의 크기, length필드

---

- 배열 객체 내에 length 필드는 배열의 크기를 나타냄

![Untitled](4%20JAVA%20%E1%84%87%E1%85%A2%E1%84%8B%E1%85%A7%E1%86%AF%208a3e7169b6054bee8ac5c6199be5637e/Untitled%201.png)

```java
// length 필드 이용 예제
// 배열의 크기 만큼 정수를 입력 받고 평균을 구하라
import java.util.Scanner;

public class ArrayLength {
	public static void main(String[] args) {
		int intArray[] = new int[5]; // 배열의 선언과 생성
		int sum=0;

		Scanner scanner = new Scanner(System.in);
		System.out.print(intArray.length + "개의 정수를 입력하세요>>");
		for(int i=0; i<intArray.length; i++)
			intArray[i] = scanner.nextInt(); // 키보드에서 입력받은 정수 저장
		
		for(int i=0; i<intArray.length; i++)
			sum += intArray[i]; // 배열에 저장된 정수 값을 더하기

		System.out.print("평균은 " + (double)sum/intArray.length);
		scanner.close();
	}
}
/* 실행 결과
5개의 정수를 입력하세요>> 2 3 4 5 9
평균은 4.6
*/
```

## 2차원 배열과 length필드

---

**2차원 배열의 모양**

![Untitled](4%20JAVA%20%E1%84%87%E1%85%A2%E1%84%8B%E1%85%A7%E1%86%AF%208a3e7169b6054bee8ac5c6199be5637e/Untitled%202.png)

**2차원 배열의 length**

- i.length → 2차원 배열의 행의 개수로서 2
- i[n].length는 n번째 행의 열의 개수
- ex) i[0].length → 0번째 행의 열의 개수로서 5

```java
// 2차원 배열 예제
// 학년별로 1,2학기 성적을 저장하고, 4년간 전체 평점 평균 출력
public class ScoreAverage {
	public static void main(String[] args) {
		double score[][] = {{3.3, 3.4},		// 1학년 1, 2학기 평점
										  {3.5, 3.6},		// 2학년 1, 2학기 평점
										  {3.7, 4.0},		// 3학년 1, 2학기 평점
										  {4.1, 4.2} };	// 4학년 1, 2학기 평점
		double sum=0;
		for(int year=0; year<score.length; year++) // 각 학년별로 반복
			for(int term=0; term<score[year].length; term++) // 각 학년의 학기별로 반복
				sum += score[year][term]; // 전체 평점 합
		
		int n=score.length; // 배열의 행 개수, 4
		int m=score[0].length; // 배열의 열 개수, 2
		System.out.println("4년 전체 평점 평균은 " + sum/(n*m));
	}
}
/*실행 결과
4년 전체 평점 평균은 3.725
*/
```