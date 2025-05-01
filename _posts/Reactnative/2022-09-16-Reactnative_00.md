---
title : "윈도우에서 React-Native 프로젝트 생성하기"
layout: single
excerpt: "React-Native APP 개발을 위한 Expo-CLI 환경설정 및 프로젝트 생성"
toc: true
toc_sticky: true
date: 2022-09-16
categories: [Reactnative]
tag: [expo]
author_profile: false
header:
  overlay_image: assets/images/header_post_1.jpg
  overlay_filter: 0.5 
---


## React Native 개발 방법   
1. React-Native-CLI   
2. Expo-CLI   
    - 해당 프로젝트는 Expo-CLI로 설정합니다. 

## 프로그램 설치     
### Node.js 설치   
10 LTS 이상 버전을 설치해야합니다. 

### VSCode 설치    
저는 프로젝트 소스코드 에디터를 주로 VScode로 사용하기 때문에   
다른 소스코드 에디터를 사용하신다면 설치하실 필요가 없습니다. 

### 모바일 expo 설치 후 계정 생성     
- 안드로이드 : `expo` APP 다운로드   
- IOS : `expo go` APP 다운로드   

### Install Expo CLI   
[윈도우 버전] : `cmd`에 해당 명령어를 입력하여 Expo를 컴퓨터에 설치해준다.   
```console
# Install the command Line tools
npm install --global expo-cli
```   

## 프로젝트 생성   

### Expo 로그인   
`cmd`에서 실행   
```console
expo login
```   
입력 후 가입한 E-mail과 PW를 입력하면 됩니다. 

### 디렉터리 이동
`cmd`에서 프로젝트를 생성할 위치로 경로 이동   
- `cd <폴더명>`    

[예시]
```console
> D:
> cd ./APPProject
```   

### expo 앱 생성
```console
expo init 프로젝트이름
```
- `blank` 선택 (expo 앱 유형)

## 프로젝트 확인 및 실행

### VS코드로 Expo 앱 확인
`cmd`에서 생성한 프로젝트의 폴더로 이동   
`cd <생성된 프로젝트 폴더명>` 으로 이동하여 프로젝트 코드 확인
```console
code .
```

### Expo 앱 실행
생성된 프로젝트 폴더의 위치에서 `cmd` 실행   
```console
# Expo 앱 실행
expo start

# Expo 앱 서버 종료
ctrl + c
```

🌞 정보 : 공부 기록용 블로그입니다. 오타나 내용 오류가 있을 경우 알려주시면 감사하겠습니다.
{: .notice}