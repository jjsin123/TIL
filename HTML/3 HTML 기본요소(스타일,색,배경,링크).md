# 3. HTML 기본요소(스타일,색,배경,링크)

Author: jk s
Category: HTML
Created Time: 2022년 11월 21일 오후 9:27
Main Category: Web
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 22일 오전 11:20

## 학습 환경

---

CodePan.io, atom.io

## **HTML 스타일(Style)**

---

HTML 요소의 style 속성(attribute)을 이용하면 CSS 스타일을 HTML 요소에 직접 설정할 수 있다. 하지만 이러한 style 속성을 이용한 방법은 오직 단 하나의 HTML 요소에만 스타일을 적용할 수 있다.

```html
<!-- 문법 -->
<태그이름 style="속성이름:속성값">
```

[https://codepen.io/jjsin123/pen/MWXQJPr](https://codepen.io/jjsin123/pen/MWXQJPr)

## **HTML 색(Color) 표현**

---

HTML에서 색을 표현하는 방법은 다음과 같이 세 가지 방법이 있다.

1. 색상 이름으로 표현(HTML에서 색상 이름은 대소문자를 구분하지 않는다.)
2. RGB 색상값으로 표현
3. 16진수 색상값으로 표현

[https://codepen.io/jjsin123/pen/abKqprX](https://codepen.io/jjsin123/pen/abKqprX)

## **HTML 배경(Background)**

---

HTML 문서의 기본 배경(background)은 흰색이다.

HTML에서는 이러한 배경을 다음과 같이 변경할 수 있다.

- 배경을 다른 색으로 변경

HTML5부터는 bgcolor 속성을 더 이상 지원하지 않으며, CSS를 이용하여 배경색을 변경하도록 하고 있다.  자세한 내용은 css 문서에서 기술한다.

- 배경을 다른 이미지로 변경

background 속성을 이용하면 HTML 요소의 배경을 이미지(image)로 설정할 수 있다.

```html
<!-- 문법 -->
<태그이름 background="이미지주소">
```

[https://codepen.io/jjsin123/pen/XWYZMWy](https://codepen.io/jjsin123/pen/XWYZMWy)

## **HTML 링크(Link)**

---

웹 페이지에는 다른 페이지나 다른 사이트로 연결되는 수많은 하이퍼 링크(hyperlink)가 존재한다.

이러한 하이퍼 링크를 간단히 링크(link)라고도 부르며, HTML에서는 `<a>`태그로 표현한다.

```html
<!-- 문법 -->
<a href="링크주소">HTML 링크</a>
```

`<a>`태그의 href 속성은 링크를 클릭하면 연결할 페이지나 사이트의 URL 주소를 명시한다.

`<a>`태그는 텍스트나 단락, 이미지 등 다양한 HTML 요소에 사용할 수 있다.

[https://codepen.io/jjsin123/pen/WNyMprX](https://codepen.io/jjsin123/pen/WNyMprX)