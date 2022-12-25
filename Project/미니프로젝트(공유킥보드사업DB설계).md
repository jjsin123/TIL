# 미니프로젝트(공유킥보드사업 DB설계)

---

![1](https://user-images.githubusercontent.com/114375741/209358956-d971d89f-bd6d-4252-8f11-a850a1ade772.jpg)

---

### 프로젝트 기획 동기

---

- 첫 프로젝트로 무엇을 해볼까 고민하던 중 데이터베이스 설계 부분을 간단한 프로젝트를 통해 더 심화적으로 학습해보고 싶어서 미니프로젝트를 진행해보았다.

### 프로젝트 소개

---

- 가상의 공유킥보드사업 공유보드(가칭)를 가정하여 킥보드정보, 대여정보, 고객정보 등을 포함한 데이터모델링 단계부터 3차 정규화까지 구현해보고 고객제공용 테이블, 데이터분석용 테이블을 따로 나누어 본다.
- 개발환경 : MariaDB, Flask
- 개발기간 : 2주

### 릴레이션 스키마

---
![Untitled](https://user-images.githubusercontent.com/114375741/209465102-c1d12ab6-ed1e-423c-b11d-94055f50f984.png)

### er 다이어그램

---
![2](https://user-images.githubusercontent.com/114375741/209358978-3c82bfc4-b63d-45c2-9917-55b7a5e92a05.jpg)

### 실행화면

---

✅ 대여 관리 페이지(대여기능, 반납)

![Untitled](https://user-images.githubusercontent.com/114375741/209359055-d73badf7-f4a8-4e09-ba46-63e030ad9a39.png)

✅ 고객 관리 페이지(추가,삭제,업데이트)

![Untitled 1](https://user-images.githubusercontent.com/114375741/209359065-c78fb79f-f323-48d4-8a8f-c99e134716b1.png)

✅ 킥보드 관리 페이지(추가,삭제,업데이트)

![Untitled 2](https://user-images.githubusercontent.com/114375741/209359066-57091682-541b-4aa6-9f3d-b3b1cfdee97e.png)

✅ 고객에게만 보여지는 고객용 뷰

![Untitled 3](https://user-images.githubusercontent.com/114375741/209359069-caf4c9f7-128f-4677-ae52-deb1595e16fd.png)
