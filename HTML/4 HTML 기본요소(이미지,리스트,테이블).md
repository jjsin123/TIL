# 4. HTML 기본요소(이미지,리스트,테이블)

Author: jk s
Category: HTML
Created Time: 2022년 11월 21일 오후 9:30
Main Category: Web
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 22일 오후 12:42

## 학습 환경

---

CodePan.io, atom.io

## **HTML 이미지(Image)**

---

이미지(image)란 2차원 평면 위에 그려진 시각적 요소를 의미한다.

웹 페이지에서 주로 사용되는 이미지의 종류는 다음과 같다.

JPEG 이미지, GIF 이미지, PNG 이미지

**이미지의 삽입**

HTML 문서에 이미지를 삽입할 때는 `<img>`태그를 사용한다.

<img>태그는 종료 태그가 없는 빈 태그(empty tag)이다.

```html
<!-- 문법 -->
<img src="이미지주소" alt="대체문자열">
```

src 속성은 이미지가 저장된 주소의 URL 주소를 명시한다.

alt 속성으로 이미지가 로딩될 수 없는 상황에서 이미지 대신 나타날 문자열을 설정할 수 있다.

**이미지의 크기(width, height) 설정**

style 속성을 사용하여 이미지의 크기를 설정할 수 있고 width 속성과 height 속성을 이용하면, 이미지의 너비와 높이를 각각 픽셀(pixel) 단위로 설정할 수도 있다. CSS를 이용하려면 style속성을 사용하는것이 좋다.

**이미지의 테두리(border) 설정**

border 속성을 사용하여 이미지의 테두리 사용 여부와 굵기를 설정할 수 있다.

**이미지에 링크(link) 설정**

이미지에 <a>태그를 이용하여 링크를 설정할 수 있다.

**이미지 맵 만들기**

HTML에서는 `<map>`태그를 이용하여 이미지 맵(image map)을 제작할 수 있다. 이미지 맵(image map)이란 이미지의 일부를 클릭할 수 있도록 만들어서 버튼처럼 사용하는 기능을 의미한다.

<img>태그의 usemap 속성을 <map>태그의 name 속성과 연결하면 이미지와 맵사이의 관계가 설정된다. <map>태그는 하나 이상의 `<area>`태그를 가지며, 이 <area>태그가 바로 버튼과 같은 역할을 한다.

[https://codepen.io/jjsin123/pen/poKaeBY](https://codepen.io/jjsin123/pen/poKaeBY)

## **HTML 리스트(List)**

---

리스트(list)란 여러 요소들을 일렬로 나열한 목록이나 명단을 의미

HTML에서는 이러한 리스트를 표현하기 위해 다음과 같은 리스트를 제공한다.

**순서가 없는 리스트**

순서가 없는 리스트는 `<ul>`태그로 시작하며, 여기에 포함되는 각각의 리스트 요소는 `<li>`태그로 시작한다.

각각의 리스트 요소 앞에는 기본 마커(marker)로 검정색의 작은 원(bullet)이 위치

**순서가 있는 리스트**

순서가 있는 리스트는 `<ol>`태그로 시작하며, 여기에 포함되는 각각의 리스트 요소는 `<li>`태그로 시작한다.

각각의 리스트 요소 앞에는 기본 마커로 아라비아 숫자가 위치

**정의 리스트(description list)**

정의 리스트(description list)는 용어와 그에 대한 정의를 모아놓은 리스트로 `<dl>`태그로 시작한다.

`<dt>`태그에는 용어의 이름이 들어가고, `<dd>`태그에는 해당 용어에 대한 정의가 들어간다.

[https://codepen.io/jjsin123/pen/VwdQbZb](https://codepen.io/jjsin123/pen/VwdQbZb)

## **HTML 테이블(Table)**

---

테이블(Table)이란 여러 종류의 데이터(data)를 보기 좋게 정리하여 보여주는 표를 의미

`<table>`태그는 다음과 같은 태그들로 구성된다.

1. `<tr>` 태그는 테이블에서 열을 구분해 준다.
2. `<th>` 태그는각 열의 제목을 나타내며, 모든 내용은 자동으로 굵은 글씨에 가운데 정렬이 된다.
3. `<td>` 태그는 테이블의 열을 각각의 셀(cell)로 나누어 준다.

**테이블의 열 합치기**

colspan 속성을 사용하면 테이블의 열(column)을 합칠 수 있다.

**테이블의 행 합치기**

rowspan 속성을 사용하면 테이블의 행(row)을 합칠 수 있다.

**테이블의 열과 행 합치기**

colspan 속성과 rowspan 속성을 함께 사용하면, 더욱 복잡한 테이블도 표현할 수 있다.

**테이블의 캡션(caption) 설정**

<caption>태그를 사용하면 테이블 상단에 제목이나 짧은 설명을 붙일 수 있다.

[https://codepen.io/jjsin123/pen/mdKXmeX](https://codepen.io/jjsin123/pen/mdKXmeX)