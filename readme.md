# 인터넷 기초[04] 과제2 - 나만의 인공지능 서비스

## 개요
 - 서비스 명 : 덕새의 드라마 추천
 - 서비스 설명 : 사용자의 취향을 입력받으면, 덕새가 분석을 통해 사용자의 마음에 들만한 드라마 세 가지를 추천해 준다. 
 - 서비스 접속 주소 : [https://Park0504jh.github.io/duksung-drama](https://Park0504jh.github.io/duksung-drama)


## 서비스 구성 요소(1) - Gemini API
- 덕새의 드라마 추천은 구글의 LMM 모델인 Gemini의 API를 활용해 진행된다.
- 활용 모델 : [Gemini-2.0-flash](https://cloud.google.com/vertex-ai/generative-ai/docs/models/gemini/2-0-flash?hl=ko)
- 시스템 프롬프트 주안점
  - 드라마를 추천해주는 인공지능에게 당신은 드라마 애청자라는 역할을 부여했다
  - 추천 드라마는 세 가지로 제한했고
  - 각 드라마마다 추천해주는 이유와 간단한 줄거리 설명을 덧붙이도록 지정했다


## 서비스 구성 요소(2) - 프론트엔드
- <덕새의 드라마 추천> 서비스 페이지는 HTML, CSS, JavaScript를 사용하여 간단하게 구성하였다.
- CSS 스타일 시트는 [style.css](style.css)파일로 따로 분리하였다.
- 덕성여대의 공식 일러스트를 사용했다. <br>
<img src="./image/bird.png" width="200px" height="200px">


## 서비스 구성 요소(3) - 백엔드
- 구글 Gemini API 호출을 위한 API 키가 노출되지 않도록, 프론트엔드의 요청을 받아서 Gemini API를 호출해주는 간단한 API 백엔드를 구성하였다.
- 코드 및 구현 내용은 [https://github.com/Park0504jh/duksung-drama-api](https://github.com/Park0504jh/duksung-drama-api)를 참고한다.