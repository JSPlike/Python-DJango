# Python-DJango
Python DJango 다시 정리하기


## 기초부터 다시 시작하는 Python Django

---- 

- 시작전 몸풀기
- 아자아자! fighting

- 빅데이터 트랙 선택

- 어떤 아이디어가 있을까요?

- 아이디어 회의중

- 오늘의 공부는??

django test


### Django Login & SignUp


### 1. django-rest-knox

> 사용이유
> 한명의 사용자에게 다수의 토큰을 제공해 줄 수있다.
> DRF에서 제공해주는 토큰의 경우 여러기기에 동시 접속이 어려웠지만
> knox를 사용함으로써 여러 기기에서 동시 접속을 가능하게 해준다.


### 2. login

> Django에서 로그인 구현 




## AWS DEPLOY


#### 1. ubuntu 서버 접속

> AWS인증키를 받은 후 부터 진행

먼저 ssh를 이용해 aws서버를 접속한다.
접속한 후에 node, npm 버전을 확인해보니 너무 낮은 버전을 사용하고 있었다.

그래서 STABLE 버전을 이용하기 위하여 npm을 업데이트 해주었다.

CURL 설치
```
sudo apt-get install curl
```

PPA 추가
```
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
```

Node.js 설치
```
sudo apt-get install -y nodejs

```


## Error 발생

1. sudo apt-get install python3 ~~ 설치시

다음과 같은 에러가 발생했다.
```
E: Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), is another process using it?
```
 
터미널열고 모든 프로세스를 죽입니다.
1) sudo killall apt apt-get


진행중인 프로세스가 없다라는 메시지가 보인다면 다음의 명령어를 따라합니다.

- sudo rm /var/lib/apt/lists/lock
- sudo rm /var/cache/apt/archives/lock
- sudo rm /var/lib/dpkg/lock*

- sudo dpkg --configure -a
- sudo apt update

순서대로 진행하고 다시 설치를 해주면 완료~~!


OK
