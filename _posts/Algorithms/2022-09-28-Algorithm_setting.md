---
title : "[Snippet, VSCode, Replit] 알고리즘 개발 환경 셋팅"
layout: single
excerpt: "[Algorithm] 개발환경 Setting 세 가지 방법"
toc: true
toc_sticky: true
date: 2022-09-28
categories: [Algorithm]
tag: [Snippet, Vscode, Replit]
author_profile: false
header:
  overlay_image: assets/images/header_post_1.jpg
  overlay_filter: 0.5 
  teaser: assets/images/Algorithm.png
---

## 알고리즘 셋팅 목표

- JavaScript 를 사용하여 작성한 코드가 실행되야 한다.
- 복잡하지 않고 바로 실행할 수 있는 DevTool 이어야 한다.

## Snippet (스니펫) 사용하여 알고리즘 개발환경 셋팅

Snippet 은 반복적인 코드들을 간편하게 불러오고 실행할 수 있는 기능입니다.  
변수에 대한 엑세스를 제공, 세션 저장소/로컬 저장소 등에 값을 설정할 수 있습니다.  
Chrome 개발자 도구 소스 아래에 있는 탭에 있으며 어떠한 설치와 설정 없이 바로 사용할 수 있습니다.  
작성된 Snippet 들은 `chrome` 자체에서 저장되기 때문에 매우 간편합니다.  

> chrome 창을 열고 개발자 도구를 띄워줍니다.  
![image](https://user-images.githubusercontent.com/50590124/192797381-d4d6ebcf-3f5d-4736-abca-a50d84575e8d.png)

### 개발자 도구 창 단축키

- `F12` 버튼 클릭
- [Window 버전] `Ctrl` + `Shift` + `I` 버튼 클릭
- [Mac 버전] `cmd` + `opt` + `I`

> `DevTool` → `Source` → `Snippets`
새로운 스니펫 생성(test) → 소스 코드 작성 → 실행 (`ctrl` + `Enter`)
![image](https://user-images.githubusercontent.com/50590124/192803806-c8887d3e-e34f-43fc-b8c6-7327ef5525a0.png)

## VSCode 사용하여 알고리즘 개발환경 셋팅  

1. 먼저 Node.JS 를 다운받습니다.
[✨Node.js 다운로드 사이트✨](https://nodejs.org/)

> 설치 후 cmd 창에서 설치가 되었는지 확인하는 방법  
 `node -v`
![image](https://user-images.githubusercontent.com/50590124/192892844-2a64a843-635d-4e88-9e97-48650188a0d1.png)

2. VSCode 를 다운받습니다.
[✨VSCode 다운로드 사이트✨](https://code.visualstudio.com/download)

3. 마켓 플레이스에서 Code Runner 다운로드
![image](https://user-images.githubusercontent.com/50590124/192893886-5c5b2dac-1188-4350-be7a-321bd6c300ae.png)

4. 코드를 작성하고 실행합니다.

- OUTPUT 출력 확인 단축키 : `Ctrl` + `Alt` + `N`
![image](https://user-images.githubusercontent.com/50590124/192894101-73a22fcd-82e0-47dc-afcc-a8603b52074e.png)  
- terminal 확인 명령어 : `node` + `실행파일 이름`
![image](https://user-images.githubusercontent.com/50590124/192895181-3ff6f627-da9f-4bbd-852b-5ef2de57278f.png)   
터미널 확인 명령어는 코드 한 줄에 디버그를 걸고 확인하고 싶을 때도 사용 가능합니다.  
해당 코드에 debugger를 걸고 동일하게 명령어를 입력하면 확인이 가능합니다.

## Replit 사용하여 알고리즘 개발환경 셋팅

Replit (리플릿)은 온라인 IDE 브라우저로 50개 이상의 언어를 설치없이 코딩할 수 있는 사이트입니다.
> [✨Repl.io 바로가기✨](https://replit.com/)
![image](https://user-images.githubusercontent.com/50590124/192890982-d28432d0-9f96-4cf4-82c1-9a25e4d08753.png)

> 로그인하여 `Create`을 클릭하면 새로운 프로젝트를 생성할 수 있습니다.
![image](https://user-images.githubusercontent.com/50590124/192891665-9fa4c8ce-0e0b-48f1-83a7-4765845c0ced.png)
![image](https://user-images.githubusercontent.com/50590124/192892025-39819145-8149-4b2c-a754-d64d2f342615.png)

🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}
