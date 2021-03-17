# git 기초

> 분산버전관리시스템(DVCS)

## 로컬 저장소(repository) 설정

```bash
$git init
Initialized empty git repository in C:/Users/student/Desktop/정리/.git

(master) $
```

* `.git` 폴더가 생성되고, 여기에 git과 관련된 모든 정보들이 저장된다.

</br>

## 기본 작업 흐름

모든 작업은 `touch`명령어를 통해서 파일을 만드는 것으로 대체한다.

### 1. add

```bash
$ git add __dir__
$ git add a.txt # 특정 파일
$ git add my_folder / # 특정 폴더
$ git add a.txt b.txt # 특정 파일들
$ git add . # 현재 디렉토리(하위 디렉토리 포함)
```

* 커밋 대상 파일 목록에 추가한다.
  * Working directory의 변경사항(첫번째 통)을 Staging area(두번째 통) 상태로 변경시킨다.

#### add 이전

```bash
$ touch new.txt
$ git status
On branch master

No commits yet
# tracking X 파일들
# git으로 관리된적이 없는 파일(새로 만든 파일 등)
Untracked files:
  # 커밋이 될 것에 포함시키기 위해서는 git add 명령어를 사용..
  # => 두번째 통(Staging Area)에 담기 위해서...
  (use "git add <file>..." to include in what will be committed)
  # 파일 목록
        new.txt
        
# Staging Area에 아무것도 없지만 Working Directory 에는 존재
nothing added to commit but untracked files present (use "git add" to track)

```

#### add 이후

```bash
$ git add .
$ git status
On branch master

No commits yet
# 커밋 될 변경사항들.. 
# Staging Area 에 파일 없음 
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.txt
```

</br>

## 2. Commit

```bash
$ git commit -m 'Add new.txt'
[master 118d3e2] Add new.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 new.txt
```

* `commit` - 지금 파일 상태를 스냅샷한다.
* 커밋 메시지는 코드 변경사항(이력/버전/커밋)을 충분히 잘 나타낼 수 있도록 작성한다.
* 아래의 명령어를 통해서 지금까지 기록된 커밋을 확인할 수 있다.

#### Log

```bash
$ git log
commit 118d3e296c3d8941e9848c5f03064dd0a17586a2 (HEAD -> master)
Author: john0814 <qudwjsdl0814@naver.com>
Date:   Tue Mar 16 15:09:25 2021 +0900

    Add new.txt

$ git log --oneline
118d3e2 (HEAD -> master) Add new.txt
5f75634 C commit
203542f Second commit
62d9b36 First commit

$ git log -1
commit 118d3e296c3d8941e9848c5f03064dd0a17586a2 (HEAD -> master)
Author: john0814 <qudwjsdl0814@naver.com>
Date:   Tue Mar 16 15:09:25 2021 +0900

    Add new.txt

$ git log --oneline -1 # 1은 표시할 라인 개수를 의미
118d3e2 (HEAD -> master) Add new.txt

```

* git bash 상에서 파일 구분방법
  * 빨간색 파일 - Working Directory 
    * 커밋이 아직 되지 않은 파일
    * 커밋은 되었으나 SD에 있지 않은 파일로 구분
  * 초록색 파일 - Staging Directory > Changes to be committed