---
title : "[Git] push한 commit message 수정"
layout: single
excerpt: "git rebase"
toc: true
toc_sticky: true
date: 2022-12-20
categories: [Git]
tag: [git]
author_profile: false
header:
  overlay_image: assets/images/header_post_1.jpg
  overlay_filter: 0.5
  teaser: assets/images/git.png
---

# 이미 push한 commit message 수정
- VScode 에서 실행한다.  

1. **Terminal 에서 수정할 git 파일이 있는 폴더로 이동한다.**  

2. **Terminal에 rebase 명령어 입력**  
git rebase HEAD~[최근에 커밋한 수]

3. **편집모드로 변경 `pick → reword`**  
터미널에 위의 코드를 입력하면 텍스트 에디터 창이 뜬다.  
수정할 커밋에서 pick 을 reword 로 변경한다.  
변경 후 저장하고 창을 닫는다.  

4. **커밋 메세지 수정**  
창을 닫으면 commit_editmsg 창이 생성된다.  
여기에서 해당 커밋의 메세지를 수정하고 저장한다.  

5. **Terminal에 push 명령어 입력**  
git push --force 를 입력한다.  
원격 저장소에 변경된 커밋 메세지를 확인할 수 있다.  

🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}
