# 나의 서버 만들기

## 1. 구조
- `static` 폴더 안에 들어있는 `style.css`는 웹서버를 꾸미는 코드를 담는 파일  
- `templates` 폴더 안에 들어있는 `.html` 파일들은 로그인창, 메뉴창 등의 코드를 담은 파일  
- `main.py`는 프로그램을 실행시키는 코드를 담은 파일  

<img src="https://github.com/user-attachments/assets/ba56ab40-54e1-4681-ae96-bb55227fb8c2" width="600" />

## 2. 내부 구조 및 코드 설명

### style.css

<img src="https://github.com/user-attachments/assets/c8c23494-e1cc-4314-8716-4d36e0ed4017" width="600" />  
<img src="https://github.com/user-attachments/assets/c15fae24-dc38-41ba-9bca-6a7948620243" width="600" />
<img src="https://github.com/user-attachments/assets/12c98fd7-de3f-4e7d-9f90-1c75e8e583e5" width="600" />
<img src="https://github.com/user-attachments/assets/5ce4ccd4-cba0-40c5-af18-ef2b3f57fa85" width="600" />


| 속성명           | 설명                    | 예시 값           |
|-----------------|-------------------------|------------------|
| width           | 요소 너비 지정          | 300px, 100%, auto |
| margin          | 요소 바깥 여백 지정     | 10px auto, 0 20px |
| padding         | 요소 안쪽 여백 지정     | 10px 5px          |
| color           | 글자 색상               | #333, rgba(0,0,0,0.5) |
| font-size       | 글자 크기               | 16px,             |
| background-color| 배경 색상               | #fff, #eee        |
| position        | 위치 지정               | static, fixed, absolute |
| top             | 위치의 위쪽 좌표 지정   | 10px, 5%          |
| left            | 위치의 왼쪽 좌표 지정   | 25%, 50px         |
| transform       | 위치 보정 등 변환       | translate(-50%, -50%) |
| border-radius   | 모서리 둥글게 처리     | 10px, 50%         |
| text-align      | 텍스트 정렬            | center, left      |
| box-sizing      | 박스 크기 계산 방식     | border-box        |
| border          | 테두리 스타일          | none, solid 5px #000 |
| z-index         | 겹침 순서              | 2, 10             |
| font-weight     | 글자 굵기              | 400, bold         |
| display         | 박스 모델 타입          | inline-block, block |


### login.html

<img src="https://github.com/user-attachments/assets/268a9aef-41b9-487e-9619-37da8264e653" width="600" />
<img src="https://github.com/user-attachments/assets/1f81c7e5-533e-4a80-8731-4db98877c767" width="600" />
<img src="https://github.com/user-attachments/assets/dc6f18db-c42d-4655-be98-76ed7cec91de" width="600" />


| 코드                                                         | 설명                | 코드                                                          | 설명                |
| ---------------------------------------------------------- | ----------------- | ----------------------------------------------------------- | ----------------- |
| `<!DOCTYPE html>`                                          | HTML 문서의 시작을 나타냄  | `<html>`, `<head>`, `<body>`                                | 기본 HTML 구조를 구성함   |
| `<title>...</title>`                                       | 브라우저 탭 제목 설정      | `<link rel="stylesheet" href="...">`                        | 외부 CSS 연결         |
| `<div class="background-title">...</div>`                  | 페이지 상단 타이틀 영역     | `<div class="...">...</div>`                                | 콘텐츠를 감싸는 컨테이너     |
| `<h2>...</h2>`                                             | 섹션 제목 표시          | `<form action="..." method="post">...</form>`               | 사용자 입력 폼 전송 구조    |
| `<input type="text" ...>`                                  | 사용자 이름 입력 필드      | `<input type="email" ...>`                                  | 이메일 입력 필드         |
| `<input type="tel" ...>`                                   | 전화번호 입력 필드        | `<input type="password" ...>`                               | 비밀번호 입력 필드        |
| `<input type="password" name="confirm" ...>`               | 비밀번호 확인 입력 필드     | `<button type="submit">...</button>`                        | 폼 제출 버튼           |
| `<a href="/signup" class="signup-link">...</a>`            | 회원가입 페이지 링크       | `<p id="errorMsg">...</p>`                                  | 오류 메시지 표시 영역      |
| `<script>...</script>`                                     | 자바스크립트 코드 블록      | `addEventListener('submit', ...)`                           | 폼 제출 시 실행할 동작 등록  |
| `const pw = document.getElementById('password').value;`    | 비밀번호 입력값 가져오기     | `const confirm = document.getElementById('confirm').value;` | 확인용 비밀번호 입력값 가져오기 |
| `if (pw !== confirm) { ... }`                              | 비밀번호가 서로 다를 경우 실행 | `e.preventDefault();`                                       | 폼 전송을 중단함 (오류 방지) |
| `document.getElementById('errorMsg').textContent = "...";` | 오류 메시지를 사용자에게 보여줌 | `<form action="/logout" method="post">...</form>`           | 로그아웃을 위한 폼        |
