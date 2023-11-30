
# JavaScript

자바스크립트 코드는 브라우저로부터 3가지 유형의 객체를 제공받아 활용할 수 있음

- BOM객체
- 코어 객체
- HTML DOM 객체
    - HTML Document Object Model
    - HTML 태그 당 DOM 객체 생성
    - 태그가 출력된 모양이나 컨텐츠 제
<br>

## ✅ DomTree

- 루트 - document 객체
- 종류 - HTML 태그 종류만큼
- 태그 당 DOM객체 하나씩 생성
- **태그의 포함관계**에 따라 DOM 트리에 부모 자식 관계가 결정됨
<br>

### 🔎 HTML 태그의 요소

- 엘리먼트 이름
- 속성
- CSS 스타일
- 이벤트 리스너
- 콘텐츠
<br>

### ‼️ DOM 객체의 구성 요소 ‼️

- 프로퍼티
    - HTML태그 속성 반영
- 메소드
    - DOM객체의 멤버 함수 → 태그 제어
- 컬렉션
  - 자식 DOM 객체들의 주소를 가짐
- 이벤트 리스너
    - 태그에 작성된 이벤트 리스너 반영
- CSS스타일
    - 태그에 작성된 스타일 시트 정보 반영
    - style property 통해 html 태그 제어 가능
  
<br><br>



# ✅ DOM객체 다루기
- 객체 구분
  - `id` 속성 사용
- 객체 찾기
    - `let p = document.getElementById(”firstP”);` <br>→ id값이 “firstP”인 DOM 리턴
- css 스타일 동적 변경
    - `p.style.backgroundColor = “green”;`
- innerHTML 동적 변경
    - `p.innerHTML = “변경할 HTML”;`
  
  <br><br>

### DOM 트리에서 DOM 객체 찾기
- 태그 이름
    - `document.getElementsByTagName()`
    - 태그 이름이 같은 객체들을 모두 찾아 컬렉션 리턴
- 클래스 이름
    - `document.getElementsByClassName()`
    - 클래스 이름이 같은 객체들을 모두 찾아 컬렉션 리턴

<br>

### Document Write

- write
    - document 객체에 담긴 HTML 콘텐츠 마지막에 태그들을 추가함
    - 추가된 태그들은 DOM 객체로 변환되어 트리에 추가됨
- writeln → write에 “\n”을 덧붙여 한 칸 띄어 출력함
    - 한 줄 띄어 출력하려면 `document.write(”<br>”);`