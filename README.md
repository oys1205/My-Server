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

- `body`  
  - `background-color`: 배경색을 흰색으로 지정  
  - `font-family`: 구글 폰트(https://fonts.google.com/)에서 가져온 글씨체 지정  

- `.background-title`  
  - `position: fixed;` : 화면에서 요소를 고정 (스크롤해도 위치가 변하지 않음)  
  - `top: 5%` : 상단 기준 아래로 5% 떨어진 위치 (px도 가능)  
  - `left: 50%` : 좌측 기준 가로 너비의 50% 지점  
  - `transform: translate(-50%, -50%)` : 요소 위치 중앙 보정  
  - `font-size`: 글자 크기  
  - `color`: 글자 색  

- `.login-container`  
  - `width`: 요소의 너비  
  - `margin`: 요소 바깥쪽 간격 (위아래 100px, 좌우 자동 중앙 정렬)  
  - `padding`: 요소 안쪽 공간  
  - `background-color`: 배경색  
  - `border-radius`: 모서리를 둥글게 만드는 속성  

- `input`  
  - `width`: 입력창 너비  
  - `margin`: 입력창 바깥쪽 간격  
  - `padding`: 입력창 내부 여백  
  - `border-radius`: 입력창 모서리 둥글게  
  - `box-sizing`: 박스 크기 계산 방식 (패딩과 보더 포함)  

---
