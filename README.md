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

<img src="https://github.com/user-attachments/assets/435e9632-a089-4431-8e81-4e9fe7a77a72" width="600" />
| 코드                                                     | 설명                                                |
| ------------------------------------------------------ | ------------------------------------------------- |
| `<!DOCTYPE html>`                                      | HTML5 문서임을 선언합니다.                                 |
| `<html>`, `<head>`, `<body>`                           | 웹페이지의 구조를 이루는 기본적인 태그입니다.                         |
| `<title>Login</title>`                                 | 브라우저 탭에 표시될 제목입니다.                                |
| `<link rel="stylesheet" href="...">`                   | 외부 CSS 파일(`style.css`)을 불러와 페이지에 스타일을 적용합니다.      |
| `<div class="signup-box">`                             | 페이지 상단에 표시되는 회원가입 유도 문구입니다.                       |
| `<a href="/signup" class="signup-link">회원가입</a>`       | 회원가입 페이지(`/signup`)로 이동하는 하이퍼링크입니다.               |
| `<div class="background-title">Rani.Ko's Server</div>` | 페이지 제목처럼 보이는 텍스트입니다. 디자인상 큰 텍스트나 배경용으로 쓰일 수 있습니다. |
| `<div class="login-container">`                        | 로그인 폼 전체를 감싸는 박스입니다. 스타일 적용을 위해 사용됩니다.            |
| `<h2>Login</h2>`                                       | 로그인 박스의 제목입니다.                                    |
| `<form action="/login" method="post">`                 | 로그인 정보를 `/login` 경로로 POST 방식으로 전송합니다.             |
| `<input type="text" ...>`                              | 사용자명(아이디)을 입력하는 필드입니다.                            |
| `<input type="password" ...>`                          | 비밀번호를 입력하는 필드입니다.                                 |
| `<button type="submit">Log in</button>`                | 로그인 버튼을 눌러 폼을 제출합니다.                              |
