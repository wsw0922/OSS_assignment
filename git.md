# 깃 명령어 정리

### add, commit 
- add, commit : 파일을 저장소에 저장
- 워킹 디렉터리에서 add 를 하면 staging area, 그 후 commit을 해야 깃 디렉터리로 넘어감

<br>

커밋 정보 확인

``` 
  $ git log  // 모든 커밋 이력 확인
  $ git log --oneline   // 커밋 이력 한 줄 출력
  $ git show   // 현재 브랜치의 가장 최근 커밋 정보를 확인
  $ git show head    // 포인터가 가르키는 커밋 자세한 정보 확인
  $ git status -s    // 간략한 상태 정보(add, commit 상태)
 ```
 
 ### clone, pull, push
 - push : 서버로 올리기
 - pull : 지역 저장소로 내리기
 - git clone [복사된 주소] : 원격 저장소와 동일한 이름으로 복제

<br>

clone

```
  $ git clone [복사된 주소] [새로운 폴더명]   // 하부 폴더에 새로운 이름으로 복제
  $ git remote   // 기본 이름 origin 점검
  $ git remote -v   // 현재 git에 등록된 원격 저장소 리스트를 보여줌
```

### 지역 원격 저장소 연동
- Fork  : 타인의 깃허브 원격 저장소를 자신의 깃허브에 복제 (공개된 저장소는 소유와 관계 없이 가능)
- Pull request : 포크된 타인의 깃허브의 내용 수정을 요청하는 PR

### 브랜치
- 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어주는 기능
- 독립적으로 어떤 작업을 진행하기 위한 개념 (각각의 브랜치는 다른 브랜치의 영향을 받지 않음)

```
  // 브랜치 생성
  $ git branch
  $ git switch -c
  $ git checkout -b

  // 브랜치 이동
  $ git switch
  $ git checkout
```

```
  $ git branch                      // 저장소 목록 보기
  $ git branch -a                   // 저장소 목록 보기, 원격 포함 전체 목록

  $ git branch newBranch            // 저장소 생성
  $ git checkout -b newBranch       // 저장소 생성, 이동
  $ git switch -c newBranch         // 저장소 생성, 이동
  $ git switch newBranch            // 저장소 이동

  $ git branch -d branchName        // 저장소 삭제
  $ git branch -D branchName        // 저장소 강제 삭제

  $ git checkout branchName         // 전환, 이동
  $ git switch branchName           // 전환, 이동

  $ git checkout -                  // 이전 브랜치로 전환, 이동
  $ git switch -                    // 이전 브랜치로 전환, 이동
```

### diff

```
  $ git diff     // stagingArea와 WD 비교
  $ git diff --cached    // diff -- staged과 동일. 커밋 HEAD와 stagingArea 비교
  $ git diff HEAD    // HEAD와 WD 비교
```'

### 브랜치 병합, 충돌해결
- merge : 여러 개의 브랜치를 하나로 모음
