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
* ** [Git TIp.](#tip)**
***

</br>

<i id="config"></i>
### 환경설정
 -- git을 사용하는 `사용자 정보를 설정.`
 　`소스변경을 한 사용자`가 누구인지하는 `추적`등에 필요함.
 
| Command   			| Description
| -------   			| -----------
| `git --version`   	| git 버전 확인
| `git config`   		| git 환경설정

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
 -- 파일 `추적`, `커밋`, `발행` 등 기본적인 명령어
 
| Command   			| Description
| -------   			| -----------
| `git add`         	| git add명령을 통해 파일을 add해야 git이 추적을 시작한다.
| `git status`   		| git 파일 상태 확인 (수정된 파일이나 add할 파일이 있는지 등)
| `git commit`   		| 스테이징에 올라가있는 파일들을 커밋
| `git checkout`   		| 파일 변경내용 되돌리기
| `git reset` 	  		| git 파일 상태를 Unstage로 변경

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
$ git checkout HEAD # HEAD에 있는 정보를 기준으로 되돌림.

## git add . 등으로 스테이징된 파일을 언스테이징시킴.
git reset
git reset HEAD README
```

</br>

<i id="repository"></i>
### 저장소
| Command     | Description
| -------     | -----------
| `git init`    | 새로운 git 저장소 생성
| `git clone`   | 원격 저장소를 복제하여 저장소 생성
| `git remote`  | git 저장소명, URL관리
| `git fetch`   | 원격 저장소로부터 로컬을 동기화
| `git pull`    | 원격 저장소로부터 로컬을 동기화하고 merge
| `git push` 	  | 원격 저장소에 변경된 내용 발행

#### Example
```bash
$ git init

## example 폴더에 저장소 복제.
## 폴더명 생략가능.
$ git clone git://github.com/wonmoyang/example.git example

# 저장소명을 출력 (기본으로 origin을 많이 씀.)
$ git remote
$ git remote -v # 저장소명 + URL 출력
$ git remote add origin https://github.com/wonmoyang/example.git # URL을 원격저장소명으로 저장
$ git remote remove origin : 원격저장소명을 삭제

# 저장소 <-> 로컬 동기화
$ git fetch

# 저장소 <-> 로컬 동기화 + merge
$ git pull

# 원격저장소명이 가리키는 원격저장소로 최신 커밋상태를 업로드
$ git push - u origin master
```

</br>

<i id="tip"></i>
### Git Tip.

커밋 수정하기.
```bash
git commit -m 'initial commit' 
git add README
git commit --amend
```