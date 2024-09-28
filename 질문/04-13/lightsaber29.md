1. 아래 코드의 실행 결과를 예측하고, 오류가 발생한다면 원인을 서술하시오.
    
    ```jsx
    let b = undefined;
    console.log(b.length);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. `TypeError` (Cannot read property 'length' of undefined)
    js에서 `undefined`는 객체가 아니므로, 어떠한 프로퍼티나 메소드도 가질 수 없다.
    `length` 프로퍼티는 일반적으로 문자열이나 배열과 같은 객체에 존재하는 프로퍼티이므로
    `undefined` 값에 대해 `length` 프로퍼티를 조회하려고 하면 JavaScript 엔진은 `TypeError`를 발생시키며, 이는 `undefined`가 어떠한 프로퍼티도 지원하지 않기 때문이다.
    → 변수에 `undefined`를 의도적으로 할당했을 때 발생할 수 있는 문제.
    코드를 작성할 때는 이런 상황을 피하기 위해 초기화되지 않은 변수를 사용하거나, 필요한 경우 명시적으로 `null`을 할당하여 '값이 없음'을 보다 안전하게 표현하는 것이 좋다
    Q. 그럼 null 을 할당하게 되면 어떻게 될까?
    Q. 선언 시 자동으로 undefined 를 할당받게 되는데 그러면 할당하지 않아도 오류가 발생할까?
    (출제위치: 6장 66쪽 두번째~네번째 문단)
    </div>
    </details>
    <br>


2. 다음 코드를 보고 출력을 예상하시오.
    
    ```jsx
    let value;
    console.log(typeof value);
    
    value = null;
    console.log(typeof value);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. `undefined`, `object`
    `null`은 단지 "값이 없다"는 것을 명시적으로 표현하는 원시 값(primitive value) 중 하나이다.
    js 에서 null 은 object 타입으로 간주되는데, 이는 설계상의 오류라고 함.

    <details>
    <summary>설계상의 오류?</summary>
    <div markdown="2">
    **왜 `typeof null`은 "object"를 반환할까?**

    이 현상은 자바스크립트의 초기 버전에서 생긴 **설계상의 오류**(bug)입니다. 자바스크립트가 개발된 1990년대에는 자바스크립트의 내부적으로 값이 저장되는 방식에 따라 데이터 타입을 구분했는데, 이때 값이 객체인지 여부를 나타내기 위해 특정 비트 패턴을 사용했습니다. 당시 `null`의 값이 이러한 비트 패턴과 일치하게 되었고, 그 결과 `null`을 **잘못** 객체로 인식하게 된 것입니다.
    
    좀 더 구체적으로:
    
    - 자바스크립트의 내부에서는 각 데이터 타입이 **비트 패턴**으로 구분됩니다.
    - 객체를 나타내는 비트 패턴은 32비트 시스템에서 `000`으로 시작하는 패턴이었는데, 불행히도 `null`도 `000`으로 시작하는 패턴을 갖고 있었습니다.
    - 이 때문에 자바스크립트는 `null`을 객체로 잘못 분류하게 되었고, 그 결과 `typeof null`이 `"object"`를 반환하게 되었습니다.
    
    **왜 수정되지 않았을까?**
    
    이 버그는 초기에 발견되었지만, 자바스크립트는 웹에서 이미 광범위하게 사용되고 있었기 때문에 이를 수정하면 **역호환성**(backward compatibility) 문제가 발생할 수 있었습니다. 즉, 이미 많은 코드가 `typeof null`이 `"object"`를 반환하는 것을 전제로 작성되어 있었기 때문에, 이를 수정하면 기존 코드가 제대로 동작하지 않을 위험이 있었던 것입니다.
    
    따라서 이 버그는 수정되지 않고 자바스크립트 표준으로 남게 되었습니다.
    </div>
    </details>

    그래서 요즘에는 `null`을 직접비교 하는 것이 대안으로 제시된다

    ```jsx
    let value = null;

    if (value === null) {
        console.log("값이 null입니다.");
    }
    ```

    (출제범위: 6장 71쪽 두번째~세번째 문단)
    </div>
    </details>
    <br>

3. 다음 코드를 보고 출력을 예상하시오.
    
    ```jsx
    ('b' + 'a' + + 'a' + 'a').toLowerCase()
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. banana
    `'b' + 'a'`
    → `ba`
    `‘ba’ + + ‘a’`
    → 첫번째 + 연산자는 좌항이 문자열이므로 문자열 연결의 역할을 함
    그 다음의 + 는 우항 ‘a’와 묶어서 단항연산자
    즉 다음과 같이 표현된다. `‘ba’ + (+ ‘a’) + ‘a’`
    이 때 단항연산자는 뒤에 오는 문자열을 숫자로 변환한 후 연산을 수행하는데
    ‘a’는 숫자가 아니라 문자이므로 → NaN을 반환함
    `‘ba’ + NaN + ‘a’`
    NaN이 문자열과 더해지면 문자열로 변환됨
    `‘baNaN’ + ‘a’` 
    `toLowerCase()` 로 대문자를 모두 소문자로 변경하게 되면
    `‘banana’` 가 출력됨
    (출제범위: 7장 78쪽 7.1.3장 전체, 9장)
    </div>
    </details>
    <br>

4. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let value = "Hello";
    
    if (value) {
        console.log("참입니다.");
    } else {
        console.log("거짓입니다.");
    }
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 참입니다 가 출력
    문자열 `"Hello"`는 자바스크립트에서 true로 변환됨
    빈 문자열(`""`)이 아닌 모든 문자열은 true로 간주하므로 if 문 내 true 블럭 실행
    (출제범위: 8장 94쪽 8.2 조건문 마지막 문단)
    </div>
    </details>
    <br>

5. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let value = null;
    let result = value || "기본 값";
    console.log(result);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. “기본값” 출력
    `||` 연산자는 왼쪽 피연산자가 **false**로 평가되면 오른쪽 값을 반환
    `null`은 **false**로 평가되므로 `"기본 값"`이 출력됨
    (출제범위: 9장 118쪽 9.4 단축평가)
    </div>
    </details>
    <br>

6. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let a = 0;
    let b = 2;
    let result = a || b && 5;
    console.log(result);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 5 출력
    연산자 우선순위에 따라 `&&` 연산이 먼저 평가
    `b && 5`에서 `b`가 true이므로 5 가 반환
    그 다음 `a || 5`가 평가
    `a`는 `0`이므로 false로 평가되어 5 가 출력됨
    (출제범위: 9장 118쪽 9.4 단축평가, 91쪽 7.12 연산자 우선순위)
    </div>
    </details>
    <br>

7. 다음 코드를 보고 코드에 오류가 발생할 지 판단하고, 정상작동 한다면 출력을 예측하시오.
    
    ```jsx
    var foo = {
    	name: 'Lee',
    	name: 'Kim'
    }
    console.log(foo);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. ‘Kim’ 이 출력
    이미 존재하는 프로퍼티 키를 중복 선언하면
    나중에 선언한 프로퍼티가 먼저 선언한 프로퍼티를 덮어쓰고, 오류가 발생하지 않는다
    (출제위치: 10장 129쪽 마지막 문단)
    </div>
    </details>
    <br>

8. 다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    function changeValue(a) {
        a = 5;
    }
    
    let num = 10;
    changeValue(num);
    
    console.log(num);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 10 출력
    함수 `changeValue`에서 `a = 5`로 변경했지만, 이는 함수 내부에서만 일어나고 값은 변경되지 않음
    숫자와 같은 **기본형**은 함수로 전달될 때 **값에 의한 전달**로 동작하므로,
    `a`에 `num`의 값이 복사된 것일 뿐 원본 `num`은 변경되지 않는다
    (출제위치: 11장 142쪽 11.1.3 값에 의한 전달)
    </div>
    </details>
    <br>

9. 다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    let obj1 = { name: "subin" };
    let obj2 = obj1;
    
    obj2.name = "lightsaber29";
    
    console.log(obj1.name);
    console.log(obj2.name);
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 둘 다 lightsaber29 로 출력됨
    **객체**는 **참조에 의한 전달**로 동작한다.
    `obj1`과 `obj2`는 같은 객체를 참조하므로
    `obj2`를 수정하면, `obj1` 도 변경된다.
    결국 두 변수는 동일한 객체를 가리키고 있으므로 동일한 값을 출력합니다.
    (출제위치: 11장 151쪽 11.2.2 참조에 의한 전달)
    </div>
    </details>
    <br>

10.  다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    sayHello();
    console.log(myFunc);
    function sayHello() {
        console.log("안녕하세요!");
    }
    var myFunc = function() {
        console.log("함수 표현식입니다.");
    };
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 안녕하세요, undefined 출력
    sayHello 함수는 함수선언문 으로 함수를 선언, myFunc 는 함수표현식으로 함수를 선언
    함수 호이스팅은 함수 선언문이 코드의 선두로 끌어올려진 것처럼 동작하는 것으로
    함수를 함수 선언문 이전에 호출하면 함수 호이스팅에 의해서 호출이 가능하다.
    그러나 함수 표현식으로 함수를 정의하면 함수 호이스팅이 발생하는 것이 아니라 변수 호이스팅이 발생
    (출제위치: 12장 165쪽 전체)
    </div>
    </details>
    <br>

11.  다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    var x = 1;
    function foo() {
      var x = 10;
      bar();
    }
    function bar() {
      console.log(x);
    }
    foo();
    bar();
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 1 이 두 번 출력됨
    </div>
    </details>
    <br>