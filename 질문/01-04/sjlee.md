## 01장 - 04장 문제
<details>
<summary>Q1. 크로스 브라우징 이슈란?</summary>
<div markdown="1">
A. 다양한 브라우저와 버전에서 브라우저에 따라 웹페이지가 의도대로 동작하지 않는 것 -> 그래서 pollyfill과 트랜스파일러가 필요하다!
</div>
</details>

<details>
<summary>Q2. 자바스크립트는 인터프리터 언어인가? 컴파일 언어인가? 그리고 그 둘의 차이는 무엇인가?</summary>
<div markdown="1">
A. 인터프리터 ->
  인터프리터: 런타임시에 한 줄씩 처리되어 프로그램이 실행되는 방식 / 
  컴파일: 런타임 전에 코드 전체를 컴파일 후, 프로그램이 실행되는 방식
</div>
</details>

<details>
<summary>Q3. 트랜스파일러란??</summary>
<div markdown="1">
A. 한 프로그래밍 언어의 코드를 다른 프로그래밍 언어로 변환해주는 도구. 
  자바스크립트 내에서는 Ecmascript 버전별로 변환할 때 사용함. 대표적으로 Babel이 있다.
  크로스브라우징이슈를 야기하는 호환성을 맞출 때나 TS 컴파일 용으로 사용한다.
</div>
</details>

<details>
<summary>Q4. 아래의 콘솔에 출력되는 값은?

  ```javascript
  console.log(score); // ???
  var score; 

  console.log(point); // ???
  let point;
  ```

</summary>
<div markdown="1">
A. undefined, Reference Error
</div>
</details>

<details>
<summary>Q5. 호이스팅에 대해 설명해주세요.?</summary>
<div markdown="1">
A. 코드의 선언부가 가장 위로 끌어올려진 것처럼 동작하는 것.
- 발생가능한 문제점  
var 선언 변수의 초기화 전에 접근하여 undefined 값을 얻게 됨.
중복된 var 선언으로 인해 예상치 못한 값이 할당되거나 사용됨.
</div>
</details>

<details>
<summary>Q6. 자바스크립트에서 값의 선언과 할당은 언제 이루어지나요?</summary>
<div markdown="1">
A. 값의 선언은 런타임 전에 이루어지고 할당은 런타임 시에 이루어집니다.
  var는 선언과 초기화가 동시에 이루어지지만, 할당은 런타임 시에 이루어집니다.
</div>
</details>
