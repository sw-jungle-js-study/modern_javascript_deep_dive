### Q 1.  지인이와 연우가 응애!하고 태어난 1999년, 자바스크립트를 이용해 서버와 브라우저가 (  1  ) 방식으로 데이터를 교환할 수 있는 통신 기능인 (  2  ) 가 XMLHttpRequest라는 이름으로 등장했다.

여기서 (1)은 작업을 동시에 진행할 수 있게 하는 방식을 말한다. 주로 I/O 작업이나 오래 걸리는 작업 처리를 할 때 사용된다. 대기 없이 작업을 시작하고 끝나면 결과를 나중에 받아 처리한다.  

<details>
<summary>A : (1)과 (2)를 적으시오.</summary>
<div markdown="1">
A. (1) 비동기
    (2) Ajax
    
</div>
</details>
    
    

### Q 2.  크롬 브라우저에서 개발자 도구를 켜려고 한다. 단축키가 생각이 안나는 혜다에게 도움을 줘야한다. 참고로 혜다의 노트북에 F12키가 빠져있다.  참고로 혜다는 윈도우다.
<details>
<summary>A : 단축키를 쓰시오.</summary>
<div markdown="1">
A.  Ctrl + Shift + I    
</div>
</details>

### Q 3.  사람은 계산과 기억을 모두 뇌로 하지만, 컴퓨터는 계산하는 뇌와, 데이터를 기억하는 뇌가 따로 있다. 각각을 적으시오.
<details>
<summary>A 계산하는 뇌 :     , 기억하는 뇌 :</summary>
<div markdown="1">
A. 계산하는 뇌 :  CPU   , 기억하는 뇌 :  메모리  
</div>
</details>
    
### Q 4.  변수는 기억하고 싶은 하나의 값을 저장하기 위해 대입할 수 있는 ‘문자’ 자체를 의미한다.
<details>
<summary> A: O / X  </summary>
<div markdown="1">
A. X : 변수는 기억하고 싶은 값을 메모리에 저장하고, 저장된 값을 읽어 들여 재 사용하기 위해 확보한 메모리공간 자체 또는 그 메모리 공간을 식별하기 위해 붙인 이름을 말한다. 즉 값의 위치를 가리키는 상징적인 이름이다.
</div>
</details>
    

### Q 5.  혜다는 변수를 선언 했다. 초기화를 안해줬더니 쓰레기 값이 들어있었다!!
<details>
<summary> A: O / X  </summary>
<div markdown="1">
A. X : 자바스크립트는 암묵적으로 undefined라는 값이 할당되어 초기화 된다.
</div>
</details>

### Q 6.  코드를 보고 출력을 예상하시오. 오류가 난다면 어디서 나는지 답하시오.

```jsx
console.log(hyeda);

hyeda = cute;
var hyeda;

console.log(hyeda);
```
<details>
<summary> A: O / X  </summary>
<div markdown="1">
A. X : 첫번째 출력 undefined, 두번째 출력 cute
자바스크립트는 변수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 변수 호이스팅이 일어난다. 즉 변수 선언은 소스코드가 런타임 이전에 먼저 실행되지만 값의 할당은 소스코드가 순차적으로 실행되는 시점   인 런타임에 실행된다. 따라서 다른 언어처럼 선언을 먼저 안했다고 오류가 나진 않는다.
</div>
</details>
    
    
    
    
