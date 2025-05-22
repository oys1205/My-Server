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

### main.py

<img src="https://github.com/user-attachments/assets/9654c01a-08a0-47a2-9546-636d989650b3" width="600" />
<img src="https://github.com/user-attachments/assets/f858f16e-fc9f-4e4c-ae1f-debd2d318942" width="600" />
<img src="https://github.com/user-attachments/assets/81056e45-8896-4d2c-b7e2-356773a8c7bb" width="600" />

FastAPI + MySQL 백엔드 코드

| 코드                                                                     | 설명                                        |
| ---------------------------------------------------------------------- | ----------------------------------------- |
| `import mysql.connector`                                               | MySQL 데이터베이스와 연결하기 위한 모듈 임포트              |
| `from fastapi import FastAPI, Request, Form`                           | FastAPI의 핵심 기능 및 요청 객체, 폼 데이터를 사용하기 위한 모듈 |
| `from fastapi.responses import HTMLResponse, RedirectResponse`         | HTML 템플릿 응답과 리다이렉트 응답을 위한 클래스             |
| `from fastapi.templating import Jinja2Templates`                       | Jinja2 템플릿 엔진을 FastAPI에서 사용하기 위한 모듈       |
| `from fastapi.staticfiles import StaticFiles`                          | 정적 파일(CSS, JS 등)을 서빙하기 위한 모듈              |
| `app = FastAPI()`                                                      | FastAPI 인스턴스를 생성하여 앱 초기화                  |
| `app.mount("/static", StaticFiles(directory="static"), name="static")` | `/static` 경로로 정적 파일을 서빙 (static 폴더 사용)    |
| `templates = Jinja2Templates(directory="templates")`                   | HTML 템플릿을 저장한 디렉터리 설정 (templates 폴더 사용)   |

데이터베이스 연결 함수

| 코드                             | 설명                                       |
| ------------------------------ | ---------------------------------------- |
| `def get_db_connection():`     | 데이터베이스 연결을 위한 함수 정의                      |
| `mysql.connector.connect(...)` | MySQL 서버에 연결 (호스트, 포트, 유저, 비밀번호, DB명 지정) |

라우팅: HTML 페이지 렌더링

| 코드                                                             | 설명                                |
| -------------------------------------------------------------- | --------------------------------- |
| `@app.get("/")`                                                | 루트 경로(`/`) 접속 시 로그인 페이지 반환        |
| `@app.get("/signup")`                                          | `/signup` 경로 접속 시 회원가입 페이지 반환     |
| `@app.get("/welcome")`                                         | `/welcome` 접속 시 환영 페이지 반환         |
| `templates.TemplateResponse("파일명.html", {"request": request})` | 해당 HTML 파일을 템플릿으로 렌더링해서 클라이언트에 응답 |

회원가입 처리 로직

| 코드                                        | 설명                          |
| ----------------------------------------- | --------------------------- |
| `@app.post("/signup")`                    | 회원가입 폼 제출 시 처리              |
| `username: str = Form(...)`               | 폼에서 입력받은 데이터를 각각 변수에 저장     |
| `if password != confirm:`                 | 비밀번호와 비밀번호 확인 값이 일치하는지 확인   |
| `cursor.execute("SELECT ...")`            | 동일한 username이 이미 존재하는지 검사   |
| `cursor.fetchone()`                       | 검사 결과 중 한 행만 가져옴 (중복 여부 확인) |
| `cursor.execute("INSERT INTO users ...")` | 새로운 사용자 정보를 users 테이블에 저장   |
| `db.commit()`                             | DB에 변경 사항 커밋 (실제 저장)        |
| `cursor.close(), db.close()`              | DB 연결 해제                    |

로그인 처리 로직

| 코드                                                  | 설명                              |
| --------------------------------------------------- | ------------------------------- |
| `@app.post("/login")`                               | 로그인 폼 제출 시 처리                   |
| `cursor.execute("SELECT ...")`                      | 입력된 사용자 정보로 DB 조회               |
| `if user:`                                          | 일치하는 유저가 있으면 로그인 성공             |
| `RedirectResponse(url="/welcome", status_code=302)` | 로그인 성공 시 환영 페이지로 리다이렉트          |
| `else: return templates.TemplateResponse(...)`      | 로그인 실패 시 에러 메시지와 함께 로그인 페이지 재출력 |

로그아웃 처리

| 코드                                                | 설명                          |
| ------------------------------------------------- | --------------------------- |
| `@app.post("/logout")`                            | 로그아웃 요청 처리                  |
| `RedirectResponse(url="/login", status_code=302)` | 로그인 페이지로 리다이렉트              |
| `response.delete_cookie("session")`               | 'session' 쿠키 삭제하여 로그인 상태 해제 |

