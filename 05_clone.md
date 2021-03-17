# git clone

* github repository에서 파일을 받아오는 방법은 두가지가 있다.

### 1. *.zip 파일 다운로드

* Github의 파일을 받아올 수 있다.

![gitclone](../image/gitclone.JPG)

* 단, .git 디렉토리가 존재하지 않아 이전 버전의 내용을 확인할 수 없다.
  * 분산버전 컨트롤 시스템의 핵심!

</br>

### 2. git clone

* *.zip 파일 다운로드 하는것과 거의 동일하나 .git 디렉토리 또한 받아올 수 있다.
* 기존 working directory에서처럼 버전관리가 가능하다.

```bash
$ git clone __git_url__
```

