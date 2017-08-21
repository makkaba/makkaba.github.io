---
title: Disqus로 댓글기능 만들기
date: 2017-08-21 17:27:31
tags:
---

Disqus에서
회원가입 후 `GET STARTED`를 선택한다
'install Disqus'를 선택한다

아래처럼 아이디를 정해줍니다
{% asset_img make_shortname.png %}

플랫폼을 선택하라고 나오는데 
hexo는 없기 때문에 수동으로 설치하겠다 클릭
{% asset_img platform.png %}
그후 다 입력해서 마무리합니다.

우리의 `_config.yml` 파일에 
아래 처럼 입력합니다
``` bash
disqus_shortname: 아까정한 숏네임
```

이렇게 해주면 자동으로 댓글 기능이 완성됩니다.
왜냐하면, 현재 default 테마인 landscape에
관련된 코드들이 있기 때문입니다.
참조)
`.../layout/_partial/after_footer.ejs`

