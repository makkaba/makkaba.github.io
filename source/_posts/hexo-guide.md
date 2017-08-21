---
title: "hexo로 블로그하기"
date: 2017-08-21 16:22:54
tags:
---

hexo를 설치한다
``` bash
npm install -g hexo-cli
```

hexo를 사용해 블로그를 생성한다
``` bash
hexo init myBlog
```
myBlog라는 디렉토리 안에 파일들이 다운된다

``` bash
cd myBlog
hexo server
```

`http://localhost:4000`에 접속해서 확인한다
`컨트롤+C`로 종료한다

깃허브에 새로운 레포지토리를 생성한다
레포지토리 이름은 반드시 
"깃허브아이디.github.io"로 생성한다
![명령어](/images/create-gh-page.png)

`_config.yml` 파일에 다음과 같이 입력한다

배포용 파일을 생성하도록 한다
``` bash
hexo generate
```

깃허브 배포용 모듈을 다운받는다
``` bash
npm install hexo-deployer-git --save
```

실행하기 전에 설정을 해준다
``` bash
deploy: 
  type: git
  repo: https://github.com/아이디/아이디.github.io.git
  branch: master
```

깃허브에 배포한다
``` bash
hexo deploy
```

`아이디.github.io` 에 들어가서 확인한다

### 포스트 시작하기
새로운 포스팅을 생성한다 (영어만 쓸 것)
``` bash
hexo new "포스팅 이름"
```
![명령어](/images/hexo-new-post.png)
