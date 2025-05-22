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

| 코드                                                                               | 설명            | 코드                                                                        | 설명            |
| -------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------------------------- | ------------- |
| `<!DOCTYPE html>`                                                                | HTML5 문서임을 알림 | `<html>`                                                                  | HTML 문서의 시작   |
| `<head>`                                                                         | 문서의 메타 정보 포함  | `<title>Login</title>`                                                    | 브라우저 탭 제목     |
| `<link rel="stylesheet" href="/static/style.css">`                               | 외부 CSS 파일 연결  | `<body>`                                                                  | 페이지 본문 시작     |
| `<div class="background-title">Rani.Ko's Server</div>`                           | 상단 제목 표시      | `<div class="login-container">`                                           | 로그인 폼 감싸는 박스  |
| `<h2>Login</h2>`                                                                 | 로그인 폼 제목      | `<form action="/login" method="post">`                                    | 로그인 데이터 전송 폼  |
| `<input type="text" name="username" placeholder="Username" required>`            | 사용자 이름 입력창    | `<input type="password" name="password" placeholder="Password" required>` | 비밀번호 입력창      |
| `<button type="submit">Log in</button>`                                          | 로그인 버튼        | `<div class="signup-box">`                                                | 회원가입 유도 문구 박스 |
| `<a href="/signup" class="signup-link">회원가입</a>`                                 | 회원가입 페이지 링크   | `<form id="signupForm" method="post" action="/signup">`                   | 회원가입 데이터 전송 폼 |
| `<input type="email" name="email" placeholder="Email" required>`                 | 이메일 입력창       | `<input type="tel" name="telephone" placeholder="Telephone" required>`    | 전화번호 입력창      |
| `<input type="password" name="confirm" placeholder="Confirm Password" required>` | 비밀번호 확인 입력창   | `<p id="errorMsg" style="color:red;"></p>`                                | 오류 메시지 표시 영역  |
| `<script>`                                                                       | 자바스크립트 시작     | `addEventListener('submit', function(e) {...}`                            | 비밀번호 일치 여부 검사 |
| `<div class="signup-container">`                                                 | 회원가입 폼 감싸는 박스 | `<div class="welcome-title">Welcome to Rani's Server</div>`               | 환영 메시지 제목     |
| `<div class="menu-container">`                                                   | 메뉴 버튼 감싸는 박스  | `<h2>Menu</h2>`                                                           | 메뉴 제목         |
| `<form>`                                                                         | 버튼 그룹 폼       | `<button type="submit">About us</button>`                                 | About us 버튼   |
| `<button type="submit">Rani.Ko</button>`                                         | 본인 정보 버튼      | `<form action="/logout" method="post">`                                   | 로그아웃 처리 폼     |
| `<button type="submit">Log out</button>`                                         | 로그아웃 버튼       |                                                                           |               |
