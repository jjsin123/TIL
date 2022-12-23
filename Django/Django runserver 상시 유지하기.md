# Django runserver

Author: jk s
Category: Django
Created Time: 2022년 12월 21일 오후 5:16
Main Category: Web
Tags: 기본
Updated Time: 2022년 12월 24일 오전 12:10

## 백그라운드에서도 장고 서버 실행시키기

---

```python
Python manage.py runserver 0:80
```

서버를 실행시키기 위해서 터미널에 위와 같은 명령어를 입력해왔다.

하지만 터미널을 종료하면, 서버도 동시에 종료가 되는데 

터미널을 종료하더라도 계속 서버를 동작 시키는 방법에 대해 알아본다.

![Untitled](Django%20runserver%201bd63b204246473f9ca512e09a0fd045/Untitled.png)

1. 위와 같이 평소처럼 `Python manage.py runserver 0:80` 명령어로 서버를 실행시킨다.
2. `ctrl+z`를 눌러 해당 프로그램을 정지 시키고 shell로 돌아온다.
3. `bg` 명령어를 입력해서 백그라운드로 보낸다.
4. `disown -h` 명령어를 통해 ssh 연결이 끊어져도 해당 프로세스가 돌아가도록 한다.
5. 터미널을 종료한다.

이렇게 하면 24시간 서버가 실행된다.

추가적으로 서버를 종료 시키는 방법을 알아본다.

![Untitled](Django%20runserver%201bd63b204246473f9ca512e09a0fd045/Untitled%201.png)

1. `ps -ef | grep [manage.py](http://manage.py/)` 명령어를 치면 데몬 형태로 실행 중인 프로세스들이 보인다. 아래의 명령어와 같이 두 번째 칸에 있는 프로세스 아이디를 입력한다.
2. `kill 프로세스아이디` ex. kill 27696
3. 백그라운드에서 실행되던 서버가 종료된다.