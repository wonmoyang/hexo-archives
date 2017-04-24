---
title: Jhipster 설치
categories:
  - Development
  - Spring
tags:
  - JHipster
date: 2017-04-24 11:25:53
thumbnail: /images/jhipster.jpg
---

{% asset_img jhipster.jpg JHipster %}

## JHipster란?
_**Jhipster**_는 _**{% link Yeoman http://yeoman.github.io [external] [yeoman] %}**_진영에서 개발된 `Angularjs + Spring boot`기반의 어플리케이션 프로젝트이다. 클라이언트, 서버측 기술들을 나열하기 힘들정도로 방대하게 제공해주고 유용한 툴이나 제공되는 개발환경 세팅이 잘되어있다.

자세한 설명은 {% link jhipster http://jhipster.github.io [external] [jhipster] %} 사이트를 참고!


## JHipster 설치 (NPM)
`Java, Nodejs, Git`등 설치가 필요하지만 여기선.. 생략 :)

```bash
## NPM Update (권장)
$ npm install -g npm

## Install Yeoman
$ npm install -g npm
```

#### `AngluarJS 1`을 설치 할 경우만 실행
```bash
# install bower (only angularjs 1)
$ npm install -g bower

# install gulk-cli (only angularjs 1)
# gulp를 이전버전으로 설치한경우 npm rm -g gulp을 실행하여 이전 버전이 gulp-cli와 충돌하지 않도록함.
$ npm install -g gulp-cli
```

install이 완료되면 마지막으로 jhipster 설치
```bash
# install JHipster
$ npm install -g generator-jhipster
```

## JHipster 프로젝트 생성
### Jhipster Quick Start
```bash
# init JHipster
$ yo jhipster
```
###### 위 커맨드를 실행하면 아래 화면이 나온다.
{% asset_img jhipster_setup(1).png yo hipster%}

```
# 어떤 유형의 어플리케이션을 만들것인지 선택
(1/15) Which *type* of application would you like to create?
> Monolithic application (recommended for simple projects) [선택]
  Microservice application
  Microservice gateway
  [BETA] JHipster UAA server (for microservice OAuth2 authentication)
```

```
# 어플리케이션 이름을 입력
(2/15) What is the base name of your application? (blog) [blog]
```

```
# JHipster Marketplace에서 다른 generator를 설치할지 여부
(3/15) Would you like to install other generators from the JHipster Marketplace? [No]
```

```
# Java 기본 Package명을 입력
(4/15) What is your default Java package name? (com.mycompany.myapp) [io.github.wonmoyang]
```

```
# 어떤 유형의 인증을 사용할것인지 선택
(5/15) Which *type* of authentication would you like to use? (Use arrow keys)
> HTTP Session Authentication (stateful, default Spring Security mechanism) [선택]
  JWT authentication (stateless, with a token)
  OAuth2 Authentication (stateless, with an OAuth2 server implementation)
```

```
# 어떤 유형의 데이터베이스를 사용할것인지 선택
(6/15) Which *type* of database would you like to use? (Use arrow keys)
> SQL (H2, MySQL, MariaDB, PostgreSQL, Oracle, MSSQL) [선택]
  MongoDB
  Cassandra
```

```
# 어떤 projection 데이터베이스를 사용할것인지 선택
? (7/15) Which *production* database would you like to use? (Use arrow keys)
> MySQL	[선택]
  MariaDB
  PostgreSQL
  Oracle (Please follow our documentation to use the Oracle proprietary driver)
```

```
# 어떤 개발 데이터베이스를 사용할것인짓 선택
(8/15) Which *development* database would you like to use? (Use arrow keys)
> H2 with disk-based persistence [선택]
  H2 with in-memory persistence
  MySQL
```

```
# Hibernate의 2 level cache 기능을 사용하지 여부
(9/15) Do you want to use Hibernate 2nd level cache? (Use arrow keys)
> No	[선택]
  Yes, with ehcache (local cache, for a single node)
  Yes, with HazelCast (distributed cache, for multiple nodes)
```

```
# backupend 빌드 시스템 선택
(10/15) Would you like to use Maven or Gradle for building the backend? (Userrow keys)
  Maven
> Gradle	[선택]
```

```
# 예외 추가설정 부분, 소셜로그인, 검색엔진, session hazelcase방식 websocket 등을 사용하려면 선택
(11/15) Which other technologies would you like to use? (Press <space> to select, 
        <a> to toggle all, <i> to inverse selection)
>( ) Social login (Google, Facebook, Twitter)
 ( ) Search engine using Elasticsearch
 ( ) Clustered HTTP sessions using Hazelcast
 ( ) WebSockets using Spring Websocket
 ( ) [BETA] Asynchronous messages using Apache Kafka
```

```
# server side framework 선택
(12/15) Which *Framework* would you like to use for the client?
  AngularJS 1.x
> [BETA] Angular 4	[선택]
```

```
# LibSass css 전 처리기 사용여부
(13/15) Would you like to use the LibSass stylesheet preprocessor for your CSS? (y/N)
```

```
# 국제화 지원여부 선택
(14/15) Would you like to enable internationalization support? (Y/n)
? Please choose the native language of the application? (Use arrow keys)
  Czech
  Danish
  Dutch
> English	[선택]
  Estonian
  French
  Galician
```

```
# 테스트 프레임워크 선택
(15/15) Besides JUnit and Karma, which testing frameworks would you like to use? (Press <space> to select, <a> to toggle all, <i> to inverse selection)
>( ) Gatling
 ( ) Cucumber
 ( ) Protractor
```