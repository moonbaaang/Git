# git config - author

커밋을 남기는 사람에 대한 정보(이메일, 이름)을 설정함

```bash
$ git config --global user.name '이름'
$ git config --global user.email '이메일@주소'
$ git config --global -l
user.email=qudwjsdl0814@naver.com
user.name=moonbaaang
```

* github 이메일주소와 동일하게 지정하면, 커밋 기록이 github 계정과 연동되어 표기 (예 - 잔디밭)
* 주의사항
  * 이 설정과 github 접근 권한과는 전혀 상관없음
    * 윈도우 - 자격 증명 관리자
    
      ![자격증명](markdown_image/%EC%9E%90%EA%B2%A9%EC%A6%9D%EB%AA%85.JPG)
    
    * 맥 - 키체인접근