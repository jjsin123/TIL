# 프로젝트(웹 사이트 구축)

---

![%EC%9B%B9%EC%82%AC%EC%9D%B4%ED%8A%B8](https://user-images.githubusercontent.com/114375741/209914051-bebb22f2-4426-45ef-857b-ba01465628aa.jpg)


### 프로젝트 기획 동기

---

- 미니 프로젝트에 이은 두번째 프로젝트로 Python, Django를 기반으로 웹사이트를 처음부터 끝까지 제작해 보고 싶어져서 프로젝트를 진행해 보았다 .
- 주요 기능으로 게시판, 블로그, 실시간 채팅, 회원가입, 로그인 기능들을 구현해보고 싶었고 추가적으로 대문페이지와,  자기소개 페이지를 마련해서 포트폴리오도 담아 보았다.
- UI 디자인적 요소보다 기능 구현면에 초점을 두고 개발을 진행하였다.

### 깃허브 & 도메인

---

- 깃허브 : [https://github.com/jjsin123/Test](https://github.com/jjsin123/Test)
- 도메인 : [https://project-mjgjc.run.goorm.io](https://project-mjgjc.run.goorm.io/)

### 기술 및 개발 환경

---

- 사용 언어 : Python , HTML, CSS, JavaScript
- 웹 프레임워크 : Django
- 서버 : Nginx
- DB : SQLite3
- 버전 관리 : git
- 기타 모듈 : channels, markdownx, crispy_forms, Redis
- 사용 툴 : goormIDE, Pycharm, google OAuth Client, cmder, docker

### 개발 기간

---

- 개발기간 : 2022.11~12

### 시스템 구성도

---

![Web_%EC%8B%9C%EC%8A%A4%ED%85%9C_%EA%B5%AC%EC%84%B1%EB%8F%84_%EC%B5%9C%EC%A2%85](https://user-images.githubusercontent.com/114375741/209914096-ab853c2c-4dc8-47c8-98bc-a522f27638f3.jpg)


### ER 다이어그램

---


![django_erd](https://user-images.githubusercontent.com/114375741/209914125-d85949ab-0bd9-4e2c-9004-243573bd3286.png)


### 기능 설명

---

- 회원가입 (email 가입, google연동 가입)
- 로그인
- 블로그 페이지
    - Create Post (로그인 한 회원에 한해서 Create 버튼 출력 됨, 이미지 또는 파일 업로드 가능, 이미지를 업로드 하지 않을 시 무작위 이미지를 생성 후 적용, Post 내용은 MarkDown형식으로 입출력 가능, 카테고리 추가, 태그 추가 가능, 등록시 자동으로 작성자, 작성시간 출력, 뒤로가기 버튼 출력)
    - Edit Post (Post를 등록한 회원에 한해서 Edit 버튼 출력, 기능은 Create와 동일)
    - Delete Post (Post를 등록한 회원에 한해서 Delete 버튼 출력, Post 삭제-삭제 시 정말 삭제 할 것인지 확인 창 출력)
    - Comment (회원에 한해서 작성가능, 비회원일시 Log in and Leave a Comment 문구 출력 후 로그인 창으로 이동, 댓글 작성자에 한 해서 댓글 수정, 삭제버튼 출력, 삭제 시 정말 삭제 할 것인지 확인 창 출력)
    - 그 외의 기능 : 카테고리(추가,삭제), 태그(추가,삭제), Post검색(제목, 태그로 검색 가능), 한 페이지당 포스트 5개씩 등록가능, 초과시 이전,다음 페이지 페이징 네이션가능
- 게시판 페이지
    - 글쓰기 (로그인 한 회원에 한해서 글쓰기 버튼 출력 됨, 글 내용은 MarkDown형식으로 입출력 가능, 등록시 자동으로 작성자, 작성시간 출력, 게시글 작성 후 뒤로가기 버튼 출력)
    - 게시글 수정 (게시글을 작성 한 회원에 한해서 게시글 수정 버튼 출력, 기능은 글쓰기와 동일)
    - 게시글 삭제 (게시글을 등록한 회원에 한해서 게시글 삭제 버튼 출력, 게시글 삭제 시 정말 삭제 할 것인지 확인 창 출력)
    - 댓글 남기기 (회원에 한해서 작성가능, 비회원일시 로그인 후 댓글을 남겨보세요 문구 출력 후 로그인 창으로 이동, 댓글 작성자에 한 해서 댓글 수정, 삭제버튼 출력, 삭제 시 정말 삭제 할 것인지 확인 창 출력)
    - 그 외의 기능 : 한 페이지당 게시글 10개씩 등록가능, 초과시 이전,다음 페이지 페이징네이션 가능
- 실시간채팅(Channels)
    - 채팅방 생성
    - 입장한 채팅방에서 실시간 채팅 이용
    - 현재 오류 발생하여 수정 중

### 실행 화면

---

✅ 대문 페이지

![대문페이지.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/%25EB%258C%2580%25EB%25AC%25B8%25ED%258E%2598%25EC%259D%25B4%25EC%25A7%2580.png)

1. navbar 2. 관리자 권한이 있는 계정은 Admin 버튼 출력 3. 비회원이면 Login 버튼, 회원이면 계정명 출력 4. 대문 소개 문구 5. 최근 블로그 Post 미리보기 6. footer

✅ Blog List

![블로그리스트페이지.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/%25EB%25B8%2594%25EB%25A1%259C%25EA%25B7%25B8%25EB%25A6%25AC%25EC%258A%25A4%25ED%258A%25B8%25ED%258E%2598%25EC%259D%25B4%25EC%25A7%2580.png)

1. 회원 계정일시 New Post 버튼 출력 2. 검색 기능(글 제목, Tag로 검색) 3. 카테고리 사이드바 4. Post 상세 보기 버튼

✅ Create Post

![CreatePost페이지.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/CreatePost%25ED%258E%2598%25EC%259D%25B4%25EC%25A7%2580.png)

✅ Blog datail

![블로그디테일페이지1.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/%25EB%25B8%2594%25EB%25A1%259C%25EA%25B7%25B8%25EB%2594%2594%25ED%2585%258C%25EC%259D%25BC%25ED%258E%2598%25EC%259D%25B4%25EC%25A7%25801.png)

✅ ****************Board List

![boardlist.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/boardlist.png)

✅ Board Detail

![boarddetail.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/boarddetail.png)

✅ Chat

Nginx로 사용시 문제가 발생하여 수정 중 추후 업로드 예정

✅ About me

![aboutme.PNG](%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%8C%E1%85%A6%E1%86%A8%E1%84%90%E1%85%B3(%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%20%E1%84%80%E1%85%AE%E1%84%8E%E1%85%AE%E1%86%A8)%202bf1c3e1717d4544b9d21b6bd1413b7c/aboutme.png)

### 라이센스

---

“This project is licensed under the terms of the **GNU General Public License v3.0** license.”

**[GNU General Public License v3.0](https://github.com/jjsin123/Test/blob/add-license-1/LICENSE)**

### 기여자 정보

---

신종규

- 깃허브 : [@jjsin123](https://github.com/jjsin123)
- 이메일 : jjsin123@naver.com
