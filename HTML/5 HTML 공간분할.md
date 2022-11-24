# 5. HTML 공간분할

Author: jk s
Created Time: 2022년 11월 24일 오후 4:47
Updated Time: 2022년 11월 24일 오후 5:12

## 학습 환경

---

CodePan.io, atom.io

## 블록과 인라인

---

**HTML 요소의 타입**

- HTML의 모든 요소는 해당 요소가 웹 브라우저에 어떻게 보이는가를 결정짓는 display 속성을 가진다.
- 대부분의 HTML 요소는 이러한 display 속성값으로 다음 두 가지 값 중 하나를 가지게 된다.
1. 블록(block)
2. 인라인(inline)

**블록(block) 타입의 요소**

- display 속성값이 블록(block)인 요소는 언제나 새로운 라인(line)에서 시작하며, 해당 라인의 모든 너비를 차지한다.
- `<p>`, `<div>`, `<h>`, `<ul>`, `<ol>`, `<form>`요소는 display 속성값이 블록(block)인 대표적인 요소이다.

**<div>요소**

- `<div>`요소는 다른 HTML 요소들을 하나로 묶는 데 자주 사용되는 대표적인 블록(block) 요소이다.
- `<div>`요소는 주로 여러 요소들의 스타일을 한 번에 적용하기 위해 사용된다.

[https://codepen.io/jjsin123/pen/rNKdRYm](https://codepen.io/jjsin123/pen/rNKdRYm)

**인라인(inline) 타입의 요소**

- display 속성값이 인라인(inline)인 요소는 새로운 라인(line)에서 시작하지 않는다. 또한, 요소의 너비도 해당 라인 전체가 아닌 해당 HTML 요소의 내용(content)만큼만 차지한다.
- `<span>`, `<a>,` `<img>`요소는 display 속성값이 인라인(inline)인 대표적인 요소이다.

**<span>요소**

- `<span>`요소는 텍스트(text)의 특정 부분을 묶는 데 자주 사용되는 인라인(inline) 요소이다.
- `<span>`요소는 주로 텍스트의 특정 부분에 따로 스타일을 적용하기 위해 사용된다.

[https://codepen.io/jjsin123/pen/wvXmOyv](https://codepen.io/jjsin123/pen/wvXmOyv)

## **iframe 요소**

---

- iframe이란 inline frame의 약자다.
- iframe 요소를 이용하면 해당 웹 페이지 안에 어떠한 제한 없이 또 다른 하나의 웹 페이지를 삽입할 수 있다.
- iframe 요소는 frame 요소와는 달리 종료 태그가 존재
- iframe 요소는 명시된 크기로 삽입되는 창의 크기가 고정

```html
<!-- 문법 -->
<iframe src="삽입할페이지주소"></iframe>
```

**iframe 요소의 테두리 변경**

- iframe 요소는 기본적으로 검정색 테두리(border)를 가진다.
- 테두리의 스타일은 style 속성에서 border 속성을 이용하면 변경할 수 있다.
- 테두리를 표현하고 싶지 않으면 style 속성에서 border 속성값을 none으로 설정하면 된다.

**iframe 요소의 페이지 변경하기**

- `<a>`태그를 이용하면 iframe 요소의 최초 페이지를 중간에 변경 가능하다.
- `<a>`태그의 target 속성과 iframe 요소의 name 속성을 연결하면, `<a>`태그를 통해 iframe 요소의 페이지를 변경할 수 있게 된다.

[https://codepen.io/jjsin123/pen/dyKmrjg](https://codepen.io/jjsin123/pen/dyKmrjg)

## 레이아웃

---

**HTML 레이아웃(Layout)**

- 레이아웃(layout)이란 특정 공간에 여러 구성 요소를 보기 좋게 효과적으로 배치하는 작업을 의미한다.
- HTML에서는 다음과 같은 방법으로 레이아웃을 작성할 수 있다.
1. div 요소를 이용한 레이아웃
2. HTML5 레이아웃
3. table 요소를 이용한 레이아웃(현재는 거의 사용X)

**div 요소를 이용한 레이아웃**

- div 요소는 CSS 스타일을 손쉽게 적용할 수 있으므로, 레이아웃을 작성하는데 자주 사용된다.

[https://codepen.io/jjsin123/pen/bGKvZOV](https://codepen.io/jjsin123/pen/bGKvZOV)

**HTML5 레이아웃**

- HTML5에서는 웹 페이지의 레이아웃만을 위한 별도의 새로운 요소들을 제공한다.

![Untitled](https://user-images.githubusercontent.com/114375741/203728671-cd7adc34-ffb8-4692-bab4-64cb4943f4e1.png)

![Untitled 1](https://user-images.githubusercontent.com/114375741/203728669-1dc8faa2-eaca-4106-a171-a355c838146d.png)

[https://codepen.io/jjsin123/pen/rNKdRoY](https://codepen.io/jjsin123/pen/rNKdRoY)
