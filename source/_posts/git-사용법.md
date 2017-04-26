---
title: git 명령어
categories:
  - Tool
  - Github
tags:
  - Github
thumbnail: 
date: 2017-04-17 14:58:02
---

{% asset_img git.png git %}

</br>

## INDEX
***
* ** [환경설정](#config)**
* ** [기본](#basic)**
* ** [저장소](#repository)**
***

</br>

<i id="config"></i>
### 환경설정
 -- git을 사용하는 `사용자 정보를 설정.`
 　`소스변경을 한 사용자`가 누구인지하는 `추적`등에 필요함.
 
| Command   		| Description
| -------   		| -----------
| git \--version   	| git 버전 확인
| git config   		| git 환경설정

#### Example
```bash
$ git --version

## git 환경변수 보기
$ git config --global --list
## 사용자 명 변경
$ git config --global user.name "wonmoyang"
## 사용자 메일 변경
$ git config --global user.email "yangwm89@gmail.com"
## git 메세지 color 변경
$ git config --global color.ui "auto"
```

</br>

<i id="basic"></i>
### 기본
 -- 파일 추적, 커밋, 발행 등 기본적인 명령어
 
| Command   		| Description
| -------   		| -----------
| git add         	| git add명령을 통해 파일을 add해야 git이 추적을 시작한다.
| git status   		| git 파일 상태 확인 (수정된 파일이나 add할 파일이 있는지 등)
| git commit   		| 스테이징에 올라가있는 파일들을 커밋
| git checkout   	| 파일 변경내용 되돌리기

#### Example
```bash
$ git add README # 새로 생성되거나 변경된 파일을 add. (rm으로 삭제된 파일은 제외)
$ git add -u README # 이전 스테이지와 비교해서 변경된 부분만 add.
$ git add -A README # git add와 git add -u를 합한 형태 (생성,수정,삭제 모든파일을 add)

## git 파일 상태확인
$ git status

## 파일 커밋
$ git commit -a ## 추적중인 모든 변경된 파일을 commit
$ git commit -m "메세지" ## 커밋 메세지 입력 후 commit

## 파일의 변경내용을 취소, 이전 커밋상태로 되돌리기.
$ git checkout README
```

</br>

<i id="repository"></i>
### 저장소
| Command   | Description
| -------   | -----------
| git init  | 새로운 git 저장소 생성
| git clone | 원격 저장소를 복제하여 저장소 생성
#### Example
```bash
$ git init

## example 폴더에 저장소 복제.
## 폴더명 생략가능.
$ git clone git://github.com/wonmoyang/example.git example
```