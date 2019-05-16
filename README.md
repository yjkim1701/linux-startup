# linux-startup
initial setting list

# ubuntu 18 LTS

# 개발 툴 설치

## nodejs 설치 (version10)

## docker, docker-compose 설치

### apt업데이트 및 저장소 추가
```
$ sudo apt-get remove docker docker-engine docker.io
$ sudo apt-get update && sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$ sudo apt-get update && sudo apt-cache search docker-ce
```

### docker, docker-compose 설치

```
$ sudo apt-get install docker-ce
$ sudo apt install docker-compose
```

### sudo 없이 사용하도록 권한 추가

```
$ sudo apt-get install docker-ce
```

# ssh 키 생성 및 등록

```
$ ssh-key -t rsa
```
