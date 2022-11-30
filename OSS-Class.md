# 수업 내용 정리

## 1주차
**1. 오픈소스 소프트웨어 개요**
  - 소스 코드의 공개를 뜻하는 용어
  - 특징 : 전 세계의 개발자가 모여 오픈소스소프트웨어를 개발하려며 소스 코드 관리를 위한 도구와 원격 저장소 역할과 협업을 위한 서버가 필요

**2. 깃과 깃허브**
  - 깃 : 소스코드 관리를 위한 분사 버전관리시스템
  - 깃허브 : 깃 기반의 저장소 및 소프트웨어 협업 개발을 위한 웹 호스팅 서비스

<br>

## 2주차
**1. 간단한 깃, 깃허브 설명**
  - commi, push, pull, add

**2. 깃 기능**
  - 컴퓨터 파일의 변경을 추적하는 데 사용되는 버전 관리 시스템
  - 여러 개발자가 함께 작업
  - 소스 코드의 변경 사항을 추적하는 데 사용
  - 여러 개의 평형 분기를 통해 비선형 개발을 지원
  - 기록 추정, 백업 생성, 협업 지원, 분산개발, 비선형개발지원, 자유 및 오픈 소스에 적합

**3. 깃 설정과 기초 명령어**

```
 $ pwd  // 현재 폴더 확인
 $ cd // 이동
 $ mkdir dname  // 디렉터리 생성
 $ ls // 리스트보기
 $ cp a b // 복사
 $ echo 
 $ clear
 $ git init // 저장소 생성
```

```
  $ git config --global core.editor 'code --wait'    // 편집기 설정
  $ git config --global user.name "wsw0922"          // 사용자 설정
  $ git config --global user.email "woojoo0922@gmail.com"        // 사용자 설정
  $ git config --global core.autocrlf true           // 맥과 윈도우 간의 자동 변환
  $ git config --global core.safecrlf false          // 뉴라인 경고 발생 없애기
  $ git config --global init.defaultbranch main      // 브랜치 이름
```

<br>

## 3주차
1. log, show
  - log : commit history 확인
  - show : commit 자세한 정보 확인

2. status
  - status -s : 파일의 상태를 짧게 확인

3. FORK, clone
  - clone : 원격 저장소를 지역 저장소에 복제

```
  $ git clone 저장소 주소
  $ git remote 
```

4. pull
  - 현재 origin에서 기본 브랜치로 가져오기

```
  $ git pull
```

### 4주차

### 5주차

### 6주차

### 7주차

### 8주차

### 9주차

### 10주차

### 11주차

### 12주차

### 13주차
