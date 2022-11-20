# 0. HTML 시작

Author: jk s
Category: HTML
Created Time: 2022년 11월 20일 오후 8:27
Main Category: Web
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 20일 오후 9:20

## 학습 환경

---

CodePan.io, atom.io

## HTML 이란?

---

- HTML은 HyperText Markup Language의 약자이다.
- 웹 페이지는 HTML 문서라고도 불리며, HTML 태그들로 구성된다.
- 각각의 HTML 태그는 웹 페이지의 디자인이나 기능을 결정하는데 사용된다.

```html
<!-- 예제 -->
<h1>제목 1</h1>

<h2>제목 2</h2>

<h3>제목 3</h3>

<p>단락 1</p>

<p>단락 2</p>
```

## HTML 태그(tag)

---

- HTML 태그는 태그 이름을 꺾쇠 괄호(<>)로 감싸서 표현한다.
- HTML 태그는 보통 시작 태그(start tag, opening tag)와 종료 태그(end tag, closing tag)의 한 쌍으로 구성된다.
- 종료 태그는 시작 태그와 전부 똑같지만, 태그 이름 앞에 슬래시(/)가 존재한다.
- 태그에 따라 시작 태그만 있고 종료 태그가 없는 태그도 존재합니다. ex) <img> <br> <hr> 등

```html
<!-- 문법 -->
<태그이름>  // 시작 태그

</태그이름> // 종료 태그
```

## **HTML 기본 구조**

---

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8" />
        <title>My test page</title>
    </head>
    <body>
				<h1>Hello</h1>
        <p>This is my page</p>
    </body>
</html>
```

- `<!DOCTYPE html>` : 웹 브라우저에게 HTML 버전의 해석 방식을 알려주는 역할을한다.
- `<html>` : HTML 문서의 루트(root) 요소를 정의한다. 이 요소는 전체 페이지의 콘텐츠를 포함하며, 기본 요소로 알려져 있다.
- `<head>` : HTML 문서의 메타데이터(metadata)를 정의한다.
- 메타데이터(metadata)란 HTML 문서에 대한 정보(data)로 웹 브라우저에는 직접적으로 표현되지 않는 정보를 의미한다.
- 이러한 메타데이터는 <title>, <style>, <meta>, <link>, <script>, <base>태그 등을 이용하여 표현할 수 있다.
- `<meta charset="utf-8">` : 이 요소는 문서가 사용해야 할 문자 집합을 설정한다. `utf-8`로 설정하는 것이 일반적.
- `<title>` : HTML 문서의 제목(title)을 정의하며 브라우저의 탭에 이 제목이 표시된다.
- `<body>` : 웹 브라우저를 통해 보이는 내용(content) 부분이다.
- `<h1>~<h6>` : 제목(heading)을 나타낸다.
- `<p>` : 단락(paragraph)을 나타낸다.

## HTML 요소 구조

---

- HTML 요소(element)는 여러 속성을 가질 수 있으며, 이러한 속성(attribute)은 해당 요소에 대한 추가적인 정보를 제공한다. 또한, HTML 요소는 시작 태그로 시작해서 종료 태그로 끝난다.
- 속성은 HTML 요소 중에서도 언제나 시작 태그 내에서만 정의되며, 속성 이름과 속성값(value)으로 표현된다.

![Untitled](0%20HTML%20%E1%84%89%E1%85%B5%E1%84%8C%E1%85%A1%E1%86%A8%209ff8db1e9512424ca21309445f526f07/Untitled.png)

```html
<!-- 문법 -->
<태그이름 속성이름="속성값">

<!-- 예제 -->
<img src="quotes.jpg" alt="이미지가 없어요">
```

- 속성 이름은 소문자로 작성한다.
- 속성값은 따옴표로 감싼다.