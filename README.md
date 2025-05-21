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

![image](https://github.com/user-attachments/assets/12c98fd7-de3f-4e7d-9f90-1c75e8e583e5)

- `button`  
  - `width`: 100% (부모 요소 너비에 맞춤)  
  - `padding`: 10px (내부 여백)  
  - `background-color`: #83e613 (연두색 배경)  
  - `border`: 없음  
  - `color`: rgb(255, 255, 255) (글자 흰색)  
  - `font-weight`: 400 (보통 두께)  

- `.signup-box`  
  - `text-align`: center (글자 가운데 정렬)  
  - `position`: absolute (절대 위치 지정)  
  - `z-index`: 2 (겹침 순서 지정)  
  - `top`: 360px (상단에서 360px 아래 위치)  
  - `left`: 440px (좌측에서 440px 오른쪽 위치)  
  - `font-size`: 13px (글자 크기)  

- `.signup-link`  
  - `display`: inline-block (인라인 블록 요소)  
  - `color`: #0026ff (짙은 파란색)  

- `.signup-container`  
  - `width`: 400px (너비 지정)  
  - `margin`: 100px auto (위아래 100px, 좌우 자동 중앙 정렬)  
  - `border-style`: solid (실선 테두리)  
  - `border-width`: 5px (테두리 두께)  
  - `border-radius`: 10px (모서리 둥글게)  
  - `padding`: 10px (내부 여백)
  
![image](https://github.com/user-attachments/assets/5ce4ccd4-cba0-40c5-af18-ef2b3f57fa85)

- `.menu-container`  
  - `width`: 400px (박스 너비)  
  - `margin`: 100px auto (위아래 100px, 좌우 자동 중앙 정렬)  

- `.welcome-title`  
  - `position`: fixed (화면에서 고정 위치)  
  - `top`: 10px (상단에서 10px 아래 위치)  
  - `left`: 25% (좌측 기준 25% 지점)  
  - `font-size`: 50px (글자 크기)  
  - `color`: #045501bd (반투명 초록색)  

- `.menu-container` (중복 정의)  
  - `width`: 300px (박스 너비)  
  - `margin`: 10% auto (상하 10%, 좌우 중앙 정렬)  
  - `text-align`: center (텍스트 중앙 정렬)  
  - `color`: #54ce36bd (반투명 연두색) 

  ---
