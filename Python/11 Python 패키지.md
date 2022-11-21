# 11. Python 패키지

Author: jk s
Category: Python
Created Time: 2022년 11월 19일 오후 3:49
Main Category: Language
Status: 🖨 Published
Tags: 기본, 학습
Updated Time: 2022년 11월 21일 오후 9:20

## 패키지(Packages)

---

- 패키지는 모듈의 집합
- 패키지 안에 여러 모듈이 존재
- 모듈을 주제별로 분리할 때 사용
- 디렉터리와 같이 계층적인 구조로 관리
- 모듈들이 서로 포함 관계를 가지며 거대한 패키지를 가짐
- 파이썬에서는 패키지가 하나의 라이브러리

![Untitled](11%20Python%20%E1%84%91%E1%85%A2%E1%84%8F%E1%85%B5%E1%84%8C%E1%85%B5%204789e737ed74414285bb7cf825a00e60/Untitled.png)

- 패키지 구조 예제

![Untitled](11%20Python%20%E1%84%91%E1%85%A2%E1%84%8F%E1%85%B5%E1%84%8C%E1%85%B5%204789e737ed74414285bb7cf825a00e60/Untitled%201.png)

### 패키지 구성 파일

---

- __init__.py
- 파이썬 패키지를 선언하는 초기화 스크립트
- 패키지에 대한 메타데이터에 해당하는 내용 포함
- 파이썬의 거의 모든 라이브러리에 포함
- 파이썬 버전 3.3 부터는 **init**.py 파일이 없어도 패키지로 인식
- 파이썬 버전 3.3 밑의 하위 버전과 호환을 위해 **init**.py 파일 생성
- __all__이라는 리스트형의 변수에 하위 패키지의 이름을 작성
- __all__=['sub_package_1', 'sub_package_2', 'sub_package_3']