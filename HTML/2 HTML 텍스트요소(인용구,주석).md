# 2. HTML 텍스트요소(인용구,주석)

Author: jk s
Category: HTML
Created Time: 2022년 11월 20일 오후 9:51
Main Category: Web
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 20일 오후 10:31

## 학습 환경

---

CodePan.io, atom.io

## 인용구**(Quotation)**

---

- HTML에서 인용구를 표현하는 방법은 다음과 같이 두 가지로 나뉜다.
1. 짧은 인용구
2. 블록 인용구

**짧은 인용구**

- `<q>`태그(quotation)를 사용하여 표현할 수 있으며, 자동으로 앞뒤에 큰따옴표가 붙는다.

**블록 인용구**

- 길이가 긴 인용문은 `<blockquote>`태그(block quatation)를 사용하여 표현할 수 있다.

<blockquote>태그는 이러한 인용 부분을 별도의 단락으로 구분하여 나타낸다.

**축양형 표현**

- HTML에서 용어의 축약형을 표현하기 위해서는 `<abbr>`태그(abbreviation)를 사용한다.

<abbr>태그 위에 마우스를 위치시키면 title 속성에 명시한 용어의 원형이 나타난다.

**주소 표현**

- `<address>`태그를 사용하면 HTML에서 주소를 표현할 수 있습니다.

이러한 주소는 이탤릭체로 표현되며, 위아래로 약간의 공백이 자동으로 삽입됩니다.

[https://codepen.io/jjsin123/pen/YzvYQmw](https://codepen.io/jjsin123/pen/YzvYQmw)

## **주석(Comment)**

---

- 주석(comment)이란 개발자가 작성한 해당 코드에 대한 이해를 돕는 설명이나 디버깅을 위해 작성한 구문을 의미한다.
- 이러한 주석은 다른 HTML 코드와는 달리 웹 브라우저에 의해 표현되지 않는다.
- `<!-- 주석내용 -->` 형식으로 표현한다.
- 중첩주석은 불가능하다.

[https://codepen.io/jjsin123/pen/bGKarGY](https://codepen.io/jjsin123/pen/bGKarGY)