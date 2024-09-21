# 2주차 퀴즈

# ch5

<details>
<summary>1.  `A, B, C` 다음 세가지 코드 블록 뒤에는 세미콜론을 붙이지 않는다. 이러한 코드 블록은 언제나 문의 종료를 의미하는 `D`를 갖기 때문이다.</summary>
<div markdown="1">
A: if 문
B: for 문
C: 함수 선언
D: 자체 종결성
</div>
</details>

<details>
<summary>2. 자바스크립트에서 문은 무엇을 가리키나요? 어떤 역활을 하나요?</summary>
<div markdown="1">
A. 자바스크립트에서 **문(statement)**은 프로그램을 구성하는 기본 단위이자 최소 실행 단위를 가리킵니다. 문은 프로그램의 동작을 나타내며, 명령어와도 같은 역할을 합니다. 자바스크립트 프로그램은 이러한 문들의 집합으로 이루어집니다.

역할:
동작 수행: 문은 특정 동작을 수행하기 위한 명령어로, 변수 선언, 값의 할당, 함수 호출, 조건 분기, 반복 실행 등을 정의할 수 있습니다.
순차 실행: 자바스크립트는 기본적으로 문을 위에서 아래로 순차적으로 실행합니다.
제어 흐름 변경: 문을 통해 코드 실행 흐름을 제어할 수 있습니다. 예를 들어, 조건문(if 문)이나 반복문(for 문)을 사용하여 특정 조건에서 코드 블록을 실행하거나 반복할 수 있습니다.
</div>
</details>

<details>
<summary> 3. 문이 끝날 때 자동으로 컴퓨터가 세미콜론 위치를 인식하여 붙여주는 것을 무엇이라고 지칭하는가? </summary>
<div markdown="1">
A. 세미콜론 자동 삽입 기능 (ASI, Automatic Semicolon Insertion)
</div>
</details>
        
  <details>
  <summary> 3-1 발생할 수 있는 오류의 예시는? </summary>
  <div markdown="1">
  A. 세미콜론 자동 삽입 기능(ASI)은 자바스크립트에서 문법적인 오류를 피하기 위해 세미콜론을 자동으로 삽입해 주지만, 예기치 않은 동작을 초래할 수 있습니다.
  </div>
  </details>

<details>
<summary> 4. 변수는 메모리 공간을 식별하기 위해 붙인 이름이다. (O/X) </summary>
<div markdown="1">
A. O, 변수는 데이터를 저장할 메모리 공간을 식별하기 위한 이름이다
</div>
</details>

# 6장

<details>
<summary> 1. JS에서 데이터 타입이 필요한 이유 3가지를 서술하시오. </summary>
<div markdown="1">
메모리 공간의 크기 결정: 데이터를 저장하려면 해당 값이 얼마나 많은 메모리를 차지할지 결정해야 합니다. 데이터 타입에 따라 할당할 메모리의 크기가 다릅니다.

값의 해석: 메모리에서 읽어들인 데이터를 어떤 방식으로 해석할지 결정하는 것이 데이터 타입입니다. 예를 들어, 같은 2진수 값이라도 숫자로 해석할지 문자열로 해석할지 타입에 따라 달라집니다.

데이터의 안정성과 오류 방지: 변수의 타입을 명확히 구분하면 예상하지 못한 타입 간 연산을 방지하고, 프로그램의 안정성을 높여 오류를 줄일 수 있습니다. 타입
</div>
</details>

<details>
<summary> 2. 이전에 할당되어 있던 값에 대한 참조를 명시적으로 제거할 때, 변수의 값이 없다는 것을 의도적으로 명시할 때 사용하는 타입은 `?` 타입이다. </summary>
<div markdown="1">
A. null
</div>
</details>

<details>
<summary> 3. `undefined`는 변수가 선언되었지만 값이 할당되지 않은 경우에 자동으로 부여되는 값이다. (O/X) </summary>
<div markdown="1">
A. O
</div>
</details>

<details>
<summary> 4. `?` 함수는 다른 값과 충돌하지 않는 유일한 심벌 값을 생성하며, 객체의 프로퍼티 키로 사용될 수 있습니다. </summary>
<div markdown="1">
A. Symbol
</div>
</details>

# 7장
<details>
<summary> 1. `?` 연산자는 좌항과 우항의 피연산자가 같은지 비교하며, 암묵적 타입 변환을 거친 후에 값을 비교합니다. </summary>
<div markdown="1">
A. ==
</div>
</details>

<details>
<summary> 2. typeof 연산자로 null 값을 확인하면 'object'가 반환된다. (O/X) </summary>
<div markdown="1">
A. (O)
자바스크립트에서 typeof null은 'object'를 반환합니다. 이것은 자바스크립트 초기 설계 시의 오류로, null이 실제로 객체가 아님에도 불구하고 'object'로 인식됩니다.
</div>
</details>

<details>
<summary> 3. 연산자 중에서 가장 우선순위가 높은 것은 `A`이며, 연산자 결합 순서는 `B`에서 `C`로 진행됩니다. </summary>
<div markdown="1">
A: 그룹 연산자 ()
B: 좌항
C: 우항
</div>
</details>

<details>
<summary> 4. 선언하지 않은 식별자를 `typeof`로 연산했을 때 결과를 서술하시오. </summary>
<div markdown="1">
A. undefined
typeof는 선언되지 않은 식별자에 대해서도 ReferenceError를 발생시키지 않고 'undefined'를 반환합니다. 예를 들어, typeof undeclaredVariable은 'undefined'로 평가됩니다.
</div>
</details>

# 8장
<details>
<summary>  1. 레이블 문을 사용하는 경우는 어떤 상황이며, 이를 사용하는 것이 권장되지 않는 이유? </summary>
<div markdown="1">

1. 레이블 문을 사용하는 경우:

    레이블 문은 반복문이나 switch 문 같은 제어문 앞에 식별자를 붙여 특정 코드 블록을 탈출하거나 건너뛰기 위해 사용됩니다. 주로 중첩된 반복문에서 외부 반복문을 빠져나가거나 특정 지점으로 이동할 때 사용됩니다.

2. 권장되지 않는 이유:

레이블 문은 코드의 가독성을 떨어뜨리고 프로그램의 흐름을 복잡하게 만듭니다. 레이블을 사용하면 프로그램의 흐름이 예측하기 어려워지고, 유지보수가 어려워질 수 있습니다. 따라서 가급적 레이블 문을 사용하지 않고, 구조를 개선하거나 다른 제어 흐름 구조(예: return, break, continue)를 사용하는 것이 좋습니다.
</div>
</details>

<details>
<summary>  2. switch 문에서 break 문을 생략하면 어떤 일이 발생하나요? </summary>
<div markdown="1">

A. switch 문에서 break 문을 생략하면:

**폴스루(fallthrough)**가 발생합니다. 즉, break 문을 생략하면 해당 case가 일치한 후에도 그 아래의 모든 case가 실행됩니다. 이는 의도치 않은 동작을 초래할 수 있습니다.

</div>
</details>

<details>
<summary>  3. switch 문의 default에는 break 문을 실행하지 않아도 된다. (O/X) </summary>
<div markdown="1">
A. (O)
default는 switch 문의 마지막 case처럼 동작하며, 그 뒤에 코드가 더 없다면 break 문을 생략해도 상관없습니다. 그러나 다른 case가 더 있다면 의도치 않은 폴스루(fallthrough)를 방지하기 위해 break 문을 사용하는 것이 좋습니다.
</div>
</details>


# 9장
<details>
<summary> 1. 암묵적 타입 변환이 발생하는 세 가지 주요 상황을 설명하하세요. </summary>
<div markdown="1">

1. 산술 연산에서:
산술 연산자는 피연산자들이 숫자여야 하기 때문에, 자바스크립트는 피연산자가 숫자가 아닌 경우 이를 자동으로 숫자로 변환합니다.

2. 비교 연산에서:
동등 비교 연산자 ==를 사용할 때, 자바스크립트는 피연산자들의 타입이 다르면 암묵적으로 타입을 변환하여 비교합니다.

3. 논리 연산에서:
if 조건문이나 논리 연산자 (&&, ||)에서 암묵적 타입 변환이 발생하여 피연산자가 불리언 타입으로 변환됩니다.
</div>
</details>

<details>
<summary>  2. 옵셔널 체이닝 연산자(?.)와 null 병합 연산자(??)의 차이점은 무엇인가요? </summary>
<div markdown="1">

1. 옵셔널 체이닝 연산자 (?.):
옵셔널 체이닝 연산자는 좌항의 피연산자가 null 또는 undefined일 때 **undefined**를 반환하고, 그렇지 않으면 우항의 프로퍼티나 메서드를 참조합니다.

예: user?.name → user가 null 또는 undefined이면 undefined 반환, 그렇지 않으면 user.name을 반환.

2. null 병합 연산자 (??):
null 병합 연산자는 좌항의 피연산자가 null 또는 undefined일 때 우항의 값을 반환하며, 그 외의 Falsy 값(예: '', 0, false, NaN)은 좌항의 값을 그대로 반환합니다.

예: value ?? 'default' → value가 null 또는 undefined면 'default' 반환, 그렇지 않으면 value 반환.
</div>
</details>

<details>
<summary> 3. 빈 문자열(`''`), `0`, `NaN`, `null`, `undefined`는 모두 **`?`** 값으로 평가되며, 불리언 타입으로 변환되면 `?`가 된다. </summary>
<div markdown="1">
A. false
</div>
</details>

# 10장
<details>
<summary>  1. 객체는 `A`와 `B`로 구성되며, 각각 객체의 상태를 나타내고 동작을 정의한다. </summary>
<div markdown="1">
A: 프로퍼티
B: 메서드
</div>
</details>

<details>
<summary>  2. 프로퍼티 키와 값은 각각 어떤 타입을 가질 수 있나요? </summary>
<div markdown="1">
A. 
프로퍼티 키: 문자열 또는 심벌(Symbol) 타입만 가능합니다. 숫자 리터럴을 사용할 수 있지만, 자바스크립트 내부에서는 자동으로 문자열로 변환됩니다.

프로퍼티 값: 자바스크립트에서 사용할 수 있는 모든 데이터 타입을 가질 수 있습니다. 즉, 원시 값(숫자, 문자열, 불리언 등), 객체, 함수 등 모두 가능합니다.
</div>
</details>

<details>
<summary>  3. 프로퍼티 키가 `A`로 구성된 경우에는 반드시 대괄호 표기법을 사용해야 하며, 이때 프로퍼티 키는 `B`로 감싸야 한다. </summary>
<div markdown="1">
A: 숫자 또는 특수 문자
B: 문자열 또는 심벌
</div>
</details>

<details>
<summary> 4. ES6에서 변수 이름과 동일한 프로퍼티 키를 사용할 경우, `?`을 생략할 수 있으며, 이를 **프로퍼티 축약 표현**이라 부른다. </summary>
<div markdown="1">
A. 프로퍼티 키
</div>
</details>


# 11장
<details>
<summary>  1. 원시 값을 할당한 변수에 새로운 값을 재할당하면 `A`에 저장된 새로운 메모리 공간을 참조하게 되며, 원시 값은 `B` 특성을 갖는다. </summary>
<div markdown="1">
A. 새로운 값
B. 불변성
</div>
</details>

<details>
<summary>  2. 문자열은 원시 타입이므로 `A`성질을 가지며, 변경하려면 `B`해야 한다. </summary>
<div markdown="1">
A. 불변성
B. 새로운 문자열을 재할당
</div>
</details>

<details>
<summary>  3. "값에 의한 전달"과 "참조에 의한 전달"의 차이점을 설명하세요. </summary>
<div markdown="1">
A. 
값에 의한 전달: 원시 값을 갖는 변수를 다른 변수에 할당하면, 그 값이 복사되어 전달됩니다. 즉, 두 변수는 서로 독립적인 값을 가지며 한쪽의 값이 변경되더라도 다른 쪽에는 영향을 미치지 않습니다.

참조에 의한 전달: 객체를 갖는 변수를 다른 변수에 할당하면 **객체의 참조 값(메모리 주소)**이 복사되어 전달됩니다. 두 변수는 동일한 객체를 가리키기 때문에 한쪽에서 객체의 프로퍼티를 변경하면 다른 쪽에서도 동일하게 변경이 반영됩니다.

</div>
</details>

<details>
<summary>  4. 자바스크립트에서는 사실상 `A`에 의한 전달만 존재하며, 객체를 할당하면 **`B`**을 통해 동일한 객체를 참조하게 된다. </summary>
<div markdown="1">
A. 값에 의한 전달
B. 참조 값
</div>
</details>


# 12장
<details>
<summary> 1. 다음은 매개변수보다 인수가 더 많은 경우이다. 예상되는 결과 값은? </summary>
<div markdown="1">
A. 7
함수 add는 두 개의 매개변수 x와 y를 받습니다. console.log(add(2, 5, 10))에서 전달된 인수 중 첫 번째와 두 번째 인수 2와 5가 각각 x와 y에 할당되며, 세 번째 인수 10은 무시됩니다. 따라서 x + y = 2 + 5 = 7이 반환됩니다.
</div>
</details>    

    function add(x, y) {
    return x + y;
    }
    console.log(add(2, 5, 10));
    
<details>
<summary>  1- 2 이때, 초과된 인수값은 그냥 버려지는가? (O,X) </summary>
<div markdown="1">
A. O: 자바스크립트에서는 매개변수보다 인수가 더 많은 경우 초과된 인수는 무시되고, 사용되지 않습니다
</div>
</details>

<details>
<summary>  2. 다음 코드에서 생략가능한 키워드는? </summary>
<div markdown="1">
A. reurn
현재 함수 foo는 아무 값도 반환하지 않으며, return 키워드를 생략하더라도 함수는 암묵적으로 undefined를 반환합니다.
</div>
</details>

        function foo () {
    return;
    }
    console.log(foo());
    

# 13장
<details>
<summary>  1. var 키워드를 사용하면 생길 수 있는 문제 3가지를 서술하시오. </summary>
<div markdown="1">

1. 변수 호이스팅:

var 키워드로 선언된 변수는 선언이 스코프의 최상단으로 끌어올려지는(hoisting) 현상이 발생합니다. 즉, 변수를 선언하기 전에 접근할 수 있지만, 값은 undefined로 초기화됩니다. 이는 예기치 못한 동작을 초래할 수 있습니다.

2. 함수 스코프:

var는 블록 스코프가 아닌 함수 스코프를 따릅니다. 즉, if, for 같은 블록 내부에서 선언된 var 변수는 블록 외부에서도 접근할 수 있어 변수 오염의 위험이 있습니다.

3. 변수 중복 선언 가능:

var 키워드로 동일한 이름의 변수를 중복 선언할 수 있습니다. 이는 변수 재할당과 선언이 구분되지 않아 코드의 가독성을 해치고, 예기치 않은 동작을 유발할 수 있습니다.
</div>
</details>
      
<details>
<summary>  2. 다음 변수들(var1~var4)의 스코프를 나타내보시오. (line`?` ~ line`?`)</summary>
<div markdown="1">
A. 
var1: 전역 스코프 (line1 ~ 끝까지)
var2: 전역 스코프 (line3 ~ 끝까지, 전역 범위에서 접근 가능)
var3: 함수 스코프 (line7 ~ line11, foo 함수 내부에서만 접근 가능)
var4: 함수 스코프 (line9 ~ line11, bar 함수 내부에서만 접근 가능)
</div>
</details>
    
    var var1 = 1;  //line1
    if (true) {
        var var2 = 2; //line3
    }
    
    function foo() { //line6
        var var3 = 3; //line7
        function bar() {
            var var4 = 4; //line9
        }
    } //line 11
    
    
<details>
<summary>  3. var 키워드 보다 let, const 키워드를 사용하는 것이 바람직한 이유는? </summary>
<div markdown="1">

A. 
1. 블록 스코프:

let과 const는 블록 스코프를 따르므로, 특정 블록 내에서만 변수가 유효하고 외부에서는 접근할 수 없습니다. 이를 통해 변수 오염을 방지할 수 있습니다.

2. 변수 중복 선언 금지:

let과 const는 동일한 이름의 변수를 중복 선언할 수 없습니다. 이는 의도치 않은 변수 재할당을 방지하고 코드의 안정성을 높입니다.

3. 호이스팅 문제 완화:

let과 const도 호이스팅이 발생하지만, 초기화되지 않은 상태로 선언된 블록 내에서만 사용 가능하여 var의 문제를 완화합니다. 변수 선언 전에는 접근할 수 없는 **"일시적 사각지대"**가 발생하여 오류를 줄입니다.
</div>
</details>
