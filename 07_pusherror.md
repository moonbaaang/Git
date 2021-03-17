# push error

```bash
$ git push origin master
To https://github.com/moonbaaang/java.git
 ! [rejected]        master -> master (fetch first)
 # push 실패
error: failed to push some refs to 'https://github.com/moonbaaang/java.git'
# 원격 저장소 작업이 로컬저장소에 없다는 뜻
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. 
# 원격저장소 변경사항들(remote changes)를 먼저 통합시키는 것을 아마 원할 것
# 다시 push하기 전에 (git pull...?)을 하면 될 것
		You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```



### 해결방법

```bash
$ git pull origin master
```

* 커밋 메시지를 작성하는 메시지가 나타난다. (vim 환경)
  * `ESC`+`:wq`로 나갈 수 있다.
* 원격저장소의 커밋과 로컬의 커밋을 병합하는 커밋이 발생한다.
* 다시 push할 수 있다.