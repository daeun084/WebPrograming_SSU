### BOM

browser object model

JS로 브라우저를 제어하기 위해 지원되는 객체

html 내용과 관계없음

국제 표준이 없기 때문에 브라우저마다 BOM 객체들이 조금 다름

- window - 윈도우 모양 제어
- navigator - 브라우저에 대한 정보 제공
- history - 브라우저 윈도우에 로드한 URL 리스트의 히스토리 관리
- location - 윈도우에 로드된 HTML 페이지의 URL 관리
- screen - 브라우저가 실행되고 있는 스크린 장치에 대한 정보 제공

<br>

## ✅ Window

열려 있는 브라우저 윈도우나 탭 윈도우의 속성을 나타내는 객체  

윈도우마다 별도의 윈도우 객체 생성

객체가 생성되는 경우

- 브라우저가 새 웹페이지를 로드할 떄
- \<iframe\> 태그 당 하나의 window 객체 생성
- `window.open("웹 페이지 URL", "윈도우 이름", "윈도우 속성")`

<br><br>

### 윈도우 열기

`window.open(sURL, sWindowName, sFeature)`

- sURL
    - 출력할 웹 페이지 주소 문자열
- sWindowName
    - 새로 여는 윈도우의 이름 문자열**(생략 가능)**
        - `_blank` : 이름 없는 **새 윈도우**를 열어 웹 페이지 로드
        - `_parent` : 현재 윈도우의 **부모 윈도우**에 웹 페이지 로드
        - `_self` : 웹 페이지 로드
        - `_top` : **브라우저 윈도우**에 웹 페이지 로드
- sFeature
    - 윈도우의 속성을 표현하는 문자열
    - `,`로 분리해 작성, 생략 가능
  
  <br><br>

[ 빈 윈도우 생성 ]

- `window.open();`
- `window.open(””);`
- `window.open(””, “”, “”);`
- `window.open(””, null, null);`

<br><br>

### 윈도우 닫기

윈도우가 닫히면 웹 페이지와 윈도우는 함께 사라짐

`window.close();`

현재 윈도우를 닫는 코드지만 브라우저에 따라 보안의 이유로 코드가 작동하지 않는 경우가 있음

⬇️ 자신이 만든 윈도우 닫기

대부분의 브라우저에서 허용

```jsx
let win = window.open();
win.close();
```

<br><br>

### window 객체의 타이머

- 1회
    - setTimeout()/clearTimeout()
    
    ```jsx
    //1회 실행하도록 타이머 설정
    let timerID = setTimeout("timeOutCode", msec) 
    //작동중인 timerID의 타이머 해제
    clearTimeout(timerID) 
    
    //timeOutCode : js code
    ```
    
- 반복
    - setInterval()/clearInterval()
    
    ```jsx
    //무한 반복하도록 타이머 설정
    //msec : 타임아웃 지연 시간
    let timerID = setInterval("timeOutCode", msec)
    clearInterval(timerID)
    ```
    
<br><br>

### 윈도우의 위치 및 크기 조절

- `window.moveBy(5, 10);`
    - 윈도우를 오른쪽으로 5, 아래로 10픽셀 이동
- `window.moveTo(25, 10);`
    - 윈도우를 스크린의 (25, 10)위치로 이동
- `window.resizeBy(-5, 10);`
    - `resizeTo(self.outerWidth-5, self.outerHeight+10);`
    - 윈도우 크기를 5픽셀 좁게, 10픽셀 길게 조정
- `window.resizeTo(200, 300);`
    - 윈도우 크기를 200x300으로 조절


<br><br>

---

### 웹 페이지 스크롤

- `window.scrollBy(10, -15);`
    - 웹 페이지를 왼쪽으로 10픽셀, 아래로 15픽셀 스크롤
- `window,scrollTo(0, 200);`
    - 웹 페이지의 (0, 200) 좌표 부분이 현재 윈도우의 왼쪽 상단 모서리에 출력되도록 스크롤


<br>

### 웹 페이지 프린트

`window.print();`

인쇄 다이얼로그가 열림

- `onbeforeprint`
- `onafterprint`