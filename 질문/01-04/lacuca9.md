<details>
<summary>Q1. 변수에 대해 설명하시오 (키워드 : 메모리, 식별)</summary>
<div markdown="1">
A. 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 메모리 공간을 식별하기 위해 붙인 이름
</div>
</details>

<details>
<summary>Q2. 동적 타입 언어의 단점에 대해 설명하시오</summary>
<div markdown="1">
A. 변수 값을 확인하기 전에는 타입을 확신할 수 없다
   유연성은 높지만 신뢰성은 떨어진다
</div>
</details>

<details>
<summary>Q3. 블록문에 대해 설명하시오</summary>
<div markdown="1">
A. 0개 이상의문을 중괄호로 묶은 것. 자체 종결성을 갖기 때문에 세미콜론을 안 붙인다
</div>
</details>

<details>
<summary>Q4. 단축 평가가 유용할 때의 패턴을 말하시오</summary>
<div markdown="1">
A. -변수가 null 또는 undefined가 아닌지 확인하고 프로퍼티를 참조할 때 (단축 평가를 사용하면 에러x)
   - 함수 매개변수에 기본값을 설정할 때 (str = str || '';)
</div>
</details>

<details>
<summary>Q5. 
< 다음 출력의 결과를 쓰시오 >
   
var person = {

    name: 'Lee'
    
};

console.log(person.name); // ??

console.log(person[name]); // ??
</summary>

<div markdown="1">
A. Lee, ReferenceError
</div>
</details>

<details>
<summary>Q6. 객체를 변수에 할당할 때, 여러 개의 식별자가 하나의 객체를 공유할 수 있는데 이것의 문제점을 설명하시오.</summary>
<div markdown="1">
A. 하나의 변수에서 객체의 프로퍼티를 변경하면 다른 변수에서도 그 변화가 반영되기 때문에   의도치 않은 결과를 초래할 수 있다
</div>
</details>

<details>
<summary>Q6. 함수형 프로그래밍이란?</summary>
<div markdown="1">
A. 함수를 일급 객체로 취급하며, 순수 함수와 상태 불변성을 중시하는 프로그래밍 패러다임
</div>
</details>

<details>
<summary>Q7. 콜백함수, 고차함수에 대해 설명하시오</summary>
<div markdown="1">
A. - 콜백함수: 매개변수를 통해 다른 함수의 내부로 전달되는 함수
   - 고차함수: 매개변수를 통해 함수의 외부에서 콜백 함수를 전달받은 함수
</div>
</details>

<details>
<summary>Q8. 렉시컬 스코프에 대해 설명하시오</summary>
<div markdown="1">
A. - 함수 정의가 평가되는 시점에 상위 스코프가 정적으로 결정되는 것즉 함수가 어디서 호출되었는지가 아니라, 함수가 어디서 정의되었는지에 따라 해당 함수의 스코프가 결정됨
</div>
</details>

<details>
<summary>Q9. 스코프 체인에 대해 간략히 설명하고, 동작 원리를 설명하시오.</summary>
<div markdown="1">
A. - 스코프가 계층적으로 연결된 것.
   1. 변수를 참조할 때, 현재 스코프에서 해당 변수가 있는지 확인
   2. 변수가 없으면, 상위 스코프로 올라가서 찾는다.
   3. 그래도 없으면 전역 스코프까지 탐색
   4. 전역 스코프에도 없으면. ReferenceError
</div>
</details>

<details>
<summary>Q10. 함수를 사용하는 이유를 아는대로 설명하시</summary>
<div markdown="1">
A. 코드의 재사용을 위해
   
유지보수의 편의성을 높임

실수를 줄여 코드의 신뢰성을 높임

코드의 가독성을 향상

</div>
</details>

