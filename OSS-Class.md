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
**1. log, show**
  - log : commit history 확인
  - show : commit 자세한 정보 확인

**2. status**
  - status -s : 파일의 상태를 짧게 확인

**3. FORK, clone**
  - clone : 원격 저장소를 지역 저장소에 복제

```
  $ git clone 저장소 주소
  $ git remote 
```

**4. pull**
  - 현재 origin에서 기본 브랜치로 가져오기

```
  $ git pull
```

## 4주차
**1. 주요 언급**
  - Fork : 타인의 깃허브 원격 저장소를 자신의 깃허브에 복제
  - pull request : 포크된 타인의 깃허브의 내용 수정을 요청하는 끌기 요청
  - clone : 깃허브 원격 저장소를 지역 저장소로 복제해 지역과 원격을 연결
  - pull : 이후 깃허브 원격 저장소의 수정 내용을 다시 지역 저장소로 끌어오기
  - push : 이후 지역저장소의 수정 내용을 다시 원격 저장소로 올리기

**2. 주요 학습**
  - pull request
  - 깃허브 fork와 팀원, 팀 깃허브간의 PR요청

<br>

## 5주차
**1. PR**
  - 저번 주와 이어지는 내용

**2. 소스트리**
  - 소스트리 사용법

## 6주차
**1. 브랜치**
  - 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어주는 기능
  - merge로 병합
  - ~와 ^ : 특정 커밋 위치 가리킴

```
  $ git branch    // 저장소 목록 보기
  $ git branch -a    // 저장소 목록 보기, 원격 포함 전체 목록
  $ git branch <new-branch>   // 저장소 생성만
  $ git checkout -b <new-branch>     // 저장소 생성하고 이동
  $ git switch –c <new-branch>    // 저장소 생성하고 이동
  $ git branch <new-branch>    // 저장소 생성만
  $ git switch <new-branch>      // 저장소 이동
  $ git branch –d branch-name   // 저장소 삭제
  $ git branch –D branch-name   // 저장소 삭제, 강제 삭제
  $ git checkout branch-name    // 전환, 이동
  $ git switch branch-name    // 전환, 이동
  $ git checkout    // 이전 브랜치로 전환, 이동
  $ git switch    // 이전 브랜치로 전환, 이동
  $ git branch –h   // 도움말 보기 
```

**2. 브랜치 관리**
  - 5가지 브랜치 종류(main, develop, feature, release, hotfix)
  - main : 제품으로 출시되는 브랜치 배포(Release) 이력을 관리하기 위해 사용
  - develop : 다음 출시 버전을 개발하는 브랜치
  - feature : 기능을 개발하는 브랜치
  - release : 이번 출시 버전을 준비하는 브랜치
  - hotfix : 출시 버전에서 발생한 버그를 수정하는 브랜치
  - 소스트리에서 브랜치 흐름 보기

<br>

## 7주차
**1. diff**
  - diff : 파일이나 커밋 차이

```
  $ git diff    // 스테이징 파일상태와 작업 공간에서 현재 수정중인 상태 비교
  $ git diff --staged   // commit된 파일상태와 add된 파일 상태 비교
  $ git diff [비교할commit해쉬1] [비교할commit해쉬2]    // commit간의 상태 비교하기 - commit hash 이용
  $ git diff HEAD HEAD^   // commit간의 상태 비교하기 - HEAD 이용
  $ git diff [비교할branch1] [비교할branch2]    // branch간의 상태 비교하기 - HEAD 이용
```

**2. 이전 커밋으로 이동**

```
$ git checkout HEAD^    // 바로 전 단계로 이동
$ git checkout HEAD~    // 바로 전 단계로 이동
$ git checkout HEAD^^   // 2딘계 이전으로 이동
$ git checkout HEAD~~   // 2딘계 이전으로 이동
```

<br>

## 8주차

중간고사

<br>

## 9주차
**1. 임시저장**
  - git stash : 커밋할 필요 없이 파일의 변경 사항을 숨기거나 비밀리에 저장할 수 있는 강력한 도구

```
  옵션 –k | --keep-index    // SA는 저장하지 않고 그대로 놔둠 그러므로 checkout할 수 없음
  옵션 –u | --include-untracked   // 추적되지 않는 파일도 임시저장에 보관
  옵션 –p | --patch   // 변경된 모든 사항들을 저장하는 것이 아니며 대화형 프롬프트를 통해 자신이 stash에 저장할 것과 저장하지 않을 것을 지정 가능

  $ git stash
  $ git stash –m ‘메시지’
  $ git stash save
  $ git stash save ‘메시지’  // 작업 폴더와 스테이징 영역을 숨김(stash)에 저장하고 작업 폴더를 정리
  $ git stash list    // 목록 보기
  $ git stash show
  $ git stash show stash@{n}
  $ git stash show -p
  $ git stash show stash@{n} -p   // 해당 stash 항목이 생성되었을 때의 commit 자료(WD의 내용)와 임시로 저장된 stash 내용 간의 차이로 표시
  -p    // 내용의 차이까지 보이기
  $ git stash pop
  $ git stash pop stash@{n}   // 최근 또는 지정된 임시저장소 내용을 가져와 반영하고 삭제
  $ git stash apply
  $ git stash apply stash@{n}   // 최근 또는 지정된 임시저장소 내용을 가져와 반영, 작업 영역만 반영, stash 목록은 그대로
  $ git stash apply --index
  $ git stash apply --index stash@{n}   // 최근 또는 지정된 임시저장소 내용을 가져와 반영, 작업 영역과 스테이징 영역도 반영, stash 목록은 그대로
  $ git stash drop
  $ git stash drop stash@{n}    // 최근 또는 지정된 임시저장소 내용을 삭제
  $ git stash clear   // stash 목록을 모두 제거
```

<br>

## 10주차
**1. 브랜치 병합, 충돌**
  - merge : 여러 개의 브랜치를 하나로 모음
  - fast-forward : 병합할 브랜치의 조상이 기준 브랜치인 경우(일렬 상태)
  - 3-way : 브랜치 분기 후 'master'에 변경 사항이 생긴 경우
  - 충돌 발생 경우 : 파일 내용을 수정 후 저장, add한 후 커밋, 필요하면 합병된 이전 브랜치 삭제
  - 주의점 : 작업과 Stage 영역에 작업중인 파일이 없는지 꼭 확인

<br>

## 11주차
**1. 병합 rebase**
  - rebase 병합 : 명령 rebase로 base를 수정하고 다시 'fast-forward 병합’ 수행: 이 병합을 직접 다시 해야함
  - 'rebase'만 하면 'master'의 위치는 그대로 유지
  - 히스토리가 선형으로 단순해지고 좀 더 깨끗한 이력을 남김

**2. 커밋이력 수정**

```
  $ git config --global core.editor ‘code --wait’   // 최근 커밋 메시지를 설정된 편집기로 수정하는 방법
  $ git commit --amend    // 최근 커밋 메시지를 설정된 편집기로 수정하는 방법
  $ git commit --amend -m "an updated commit message“   // 최근 커밋 메시지를 직접 입력해 수정, 새로운 커밋 ID로 수정됨 
  $ git commit --amend --no-edit    // 메시지 수정 없이 다시 커밋 수정, 새로운 커밋 ID로 수정됨
```

<br>

## 12주차

**1. 버전 되돌리기**
  - reset : 특정 커밋으로 완전히 되돌아가면 해당 커밋 이후의 이력은 모두 사라지므로 주의가 필요
  - 옵션 : --hard(지정된 커밋 이력 내용으로 깃 저장소는 물론 작업 폴더와 스테이지
영역까지 이전 내용을 무시하고 모두 수정하는 작업을 수행), --mixed(지정된 커밋 이력 내용으로 깃 저장소와 스테이지 영역만 이전 내용을 무시하고 수정하는 작업을 수행), --soft( 지정된 커밋 이력 내용으로 깃 저장소만 수정하는 작업을 수행)

<br>

## 13주차

**1.reset & revert**
  - reset : 특정 커밋으로 되돌아가기(옵션 : --soft, -- mixed, --hard)
  - revert : 지정한 커밋을 취소해 바로 이전 상태로 되돌리는 방법
