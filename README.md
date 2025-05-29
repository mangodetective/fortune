## 📄 인터넷기초\[04] 과제2 - 나만의 인공지능 서비스

---

## 🧧 서비스명: **오늘의 운세**

---

## 📝 서비스 개요

**오늘의 운세**는 사용자의 이름과 생년월일을 입력받아,
그날의 운세를 **사주풀이 형식**으로 제공하는 인공지능 운세 서비스입니다.
마지막에는 **희망을 전하는 한 줄 격언**이 함께 제공되어,
보다 긍정적이고 즐거운 하루를 응원합니다. ✨

---

## 🌐 서비스 접속 주소

👉 [https://mangodetective.github.io/fortune/](https://mangodetective.github.io/fortune/)

---

## ⚙️ 서비스 구성 요소

### (1) 📡 Gemini API (백엔드 기반 LLM 운세 생성)

* **활용 모델**: `Gemini-1.5-flash`
* **시스템 프롬프트 특징**:

  * 인공지능에게 **60년 경력의 사주풀이 전문가** 역할 부여
  * 운세는 **200자 이내**로 간결하게
  * 항상 **긍정적 표현**만 포함
  * 마지막엔 반드시 **희망을 주는 한 줄 격언** 포함

---

### (2) 💻 프론트엔드 (웹 페이지)

* **구성 기술**: HTML + CSS + JavaScript
* **사용자 입력**: 이름, 생년월일 입력 폼
* **API 요청 방식**: `fetch()`를 이용한 POST 방식 API 호출
* **스타일링**: `style.css`로 별도 분리
* **결과 출력**: 운세 결과를 `div#result`에 동적으로 표시

---

### (3) ☁️ 백엔드 (서버리스 API)

* **기능**: 사용자의 입력을 바탕으로 Gemini API에 요청 후 응답 전달
* **환경**: `Vercel`의 서버리스 함수(API Routes) 기능 사용
* **보안 고려**: `GEMINI_API_KEY`는 `.env`에 숨겨서 관리

> 📁 백엔드 코드 위치:
> [https://github.com/mangodetective/duksung-fortune-api](https://github.com/mangodetective/duksung-fortune-api)