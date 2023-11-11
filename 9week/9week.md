# JAVASCRIPT
- interpret 언어 -> 컴파일 필요X <br>
웹 브라우저가 직접 소스코드를 해석해야 함
- 브라우저 위에서 실행됨
- 변수 타입 선언하지 않아도 사용 가능
- 객체지향 지원 + 함수형 프로그래밍
<br>
### ✅ HTML 문서에 JS 삽입 하기
1. 내부 <br>
   \<script\> 태그를 사용해 JS 코드 작성
        - head, body 태그 내부에 사용 가능 <br>
        - 여러 번 사용 가능
2. 외부
    `\<head\>`태그에서 `\<script\>` 태그를 통해 외부 JS 파일 불러오기
    ```html
    <head>
    <script src="myscript.js"></script>
    </head>
    ```
3. 인라인
    속성을 사용해 JS코드 직접 추가 <br>
    ```html
    <button type="button" onclick="alert('반갑습니다.')">버튼을 누르세요!</button>
    ```

<br><br>
### ✅ Dialog
- Prompt <br>
    `prompt(”메세지”, “디폴트값”)`
- Confirm <br>
    `confirm(”메세지”)`
- Alert <br>
    `alert(”메세지”)`

<br><br>
### ✅ Data Type
- 수치형
  정수, 실수
- bool
- 문자형
  char 타입 없이 <strong>String 타입만 존재 <strong><br>
  `"`, `'` 모두 사용 가능 <br>

<br><br>
### ✅ 변수
- `var`
- `let` <br>
  var 다음 등장
- `const` <br>
    상수 지정

<br>
java, c와는 다르게 int, float과 같은 타입이 존재하지 않아
변수에 어떠한 타입이라도 저장할 수 있음 <br>
<strong>저장되는 값에 제약이 없음</strong> <br>
⚠️ `int score;` -> 오류 <br>