# git config - author

* 커밋을 남기는 사람에 대한 정보(이메일, 이름)을 설정한다.

```bash
$ git config --global user.name '이름'
$ git config --global user.email '이메일@주소'
$ git config --global -l
user.email=qudwjsdl0814@naver.com
user.name=moonbaaang
```

* 위의 설정은 github 권한과는 상관이 없다.
  * 다만, github 이메일주소와 동일하게 지정하면, 커밋 기록이 github 계정과 연동되어 표기된다. (예 - 잔디밭)
* 주의사항
  * github인증 및 권한은 아래에서 관리된다.
    * 윈도우 - 자격 증명 관리자
    * 공용 계정에서는 자격 관리가 필수이다.

![자격증명](markdown_image/%EC%9E%90%EA%B2%A9%EC%A6%9D%EB%AA%85.JPG)

* 맥 - 키체인접근