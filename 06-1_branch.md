# branch

## 기본 명령어

> HEAD 정보는 커밋 히스토리 상에서 위치정보를 나타낸다.

* branch를 생성하기 전에 기본적으로 한번은 commit이 완료되어야한다.
  * 그렇지 않으면 다음과 같은 오류가 발생한다.

```bash
$ git branch A_branch
fatal: Not a valid object name: 'master'.
```

</br>

##### # 다음과 같이 branch를 생성한다.

```bash
$ git branch __branchname__
```

##### # 해당 branch로 이동한다.

```bash
$ git checkout __branchname__
Switched to branch 'A_branch'
```

* 현재 과정에서는 `__branchname__`을 `A_branch`로 작성했다.

##### # branch의 생성 및 이동을 한번에 수행할 수 있다.

```bash
$ git checkout -b __branchname__
```

##### # branch를 병합한다.

```bash
(master) $ git merge __branchname__
```

* `master` 브랜치에 `__branchname__` 을 병합

##### # branch 목록을 확인해본다.

```bash
$ git branch
  A_branch
* master
```

##### # branch를 삭제한다.

```bash
$ git branch -d __브랜치이름__
Deleted branch ppt (was ff03b20).
```

