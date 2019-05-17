# linux-startup
initial setting list

# ubuntu 18 LTS

# 시간대 변경

```
$ sudo dpkg-reconfigure tzdata
```

### vim 설치 및 설정
```
$ sudo apt-get install vim
$ cd ~
$ touch .vimrc
$ vi ~/.vimrc
```
#### vi에서 아래 내용을 작성

set number    " line 표시
set ai    " auto indent
set si " smart indent
set cindent    " c style indent
set shiftwidth=4    " 자동 공백 채움 시 4칸
set tabstop=4    " tab을 4칸 공백으로
set ignorecase    " 검색 시 대소문자 무시
set hlsearch    " 검색 시 하이라이트
set nocompatible    " 방향키로 이동 가능
set fileencodings=utf-8,euc-kr    " 파일 저장 인코딩 : utf-8, euc-kr
set fencs=ucs-bom,utf-8,euc-kr    " 한글 파일은 euc-kr, 유니코드는 유니코드
set bs=indent,eol,start    " backspace 사용가능
set ruler    " 상태 표시줄에 커서 위치 표시
set title    " 제목 표시
set showmatch    " 다른 코딩 프로그램처럼 매칭되는 괄호 보여줌
set wmnu    " tab 을 눌렀을 때 자동완성 가능한 목록
syntax on    " 문법 하이라이트 on
filetype indent on    " 파일 종류에 따른 구문 강조
set mouse=a    " 커서 이동을 마우스로 가능하도록

# 개발 툴 설치

## openjdk8 설치

```
$ sudo apt-get install openjdk-8-jdk
```

## nodejs 설치 (version10)

```
$ curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
$ sudo apt-get install -y nodejs
```

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
