# WebProgramming 11week
<br>

## ✅ JavaScript의 함수
- 함수 구성
    ```javascript
    function adder ( a,  b ) {
        let sum;
        sum = a + b;
        return sum; // 덧셈 합 리턴
    }
    ```
    <br>
- **무명 함수** <br>
    anonymous function <br>
    함수의 이름을 지정하지 않고 만들어 한 번만 사용하는 함수 <br>
    ```javascript
    let greeting = function()
	{
		alert("anonymous function");
	}

    greeting(); //함수 호출
    ```
    <br>
- **화살표 함수** <br>
    arrow function <br>
    자바의 람다식과 유사한 구조로, 함수를 더 짧게 작성하기 위해 도입됨 <br>
    ```javascript
    //기존 함수 모양
    function() sub(a, b)
    {
        return a - b;
    }
    ```
    ```javascript
    //arrow function

    //1. 
    (a, b) => { return a - b; }

    //2.
    (a, b) => return a - b;

    //3.
    (a, b) => a - b;
    ```
    <br>
- **전역함수** <br>
    JavaScript의 대표적인 전역함수
    - `eval()`
    - `isNaN()`
    - `parseInt()`

<br><br>
<hr><br><br>

# ✅객체
- 데이터와 동작을 가지고 있음
- 객체 내부의 변수→ 속성(property)
- 객체 내부의 함수 → 메소드(method)
<br><br>

### JS의 객체 구성
여러 개의 프로퍼티 + 메소드
- 내장 객체
    - **핵심객체** : Date, String, Array
    - **BOM** : 브라우저의 종류나 크기에 대해 정보 제공
    - **DOM** : 브라우저가 HTML 문서를 파싱해 각 요소들을 객체 트리로 정의
- 사용자 정의 객체
<br>

‼️ JavaScript는 **객체 기반 언어**이지 객체 지향 언어가 아님