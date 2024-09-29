1. 다음 코드를 보고, 이 코드에서 발생할 수 있는 **암묵적 결합** 문제를 해결하기 위해 코드를 수정하시오.
    
    ```jsx
    let discount = 0.1;
    
    function calculatePrice(price) {
        return price - (price * discount);
    }
    
    console.log(calculatePrice(100));
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    ```jsx
    function calculatePrice(price, discount) {
        return price - (price * discount);
    }
    console.log(calculatePrice(100, 0.1));
    ```

    전역변수 `discount` 가 함수 내부에서 사용되고 있어 암묵적 결합이 발생
    → 이를 해결하기 위해 `discount` 값을 함수의 매개변수로 전달해야함

    (출제위치: 14장 203쪽 마지막 문단)
    </div>
    </details>
    <br>

2. 다음 문장을 읽고 빈 칸에 들어갈 단어를 맞추시오.
    
    ```
    변수의 생명주기는 메모리 공간이 확보 된 시점부터
    메모리 공간이 해제 되어 _______________에 반환되는 시점까지다.
    ```

    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 가용 메모리 풀

    (출제위치: 14장 201쪽 다섯번째 문단)
    </div>
    </details>
    <br>

3. 다음 코드를 실행할 때 출력 결과를 예상하고, 발생하는 문제를 설명하시오.
    
    ```jsx
    console.log(x);
    var x = 5;
    
    console.log(y);
    let y = 5;
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. undefined, ReferenceError 발생

    `var`로 선언된 변수는 **호이스팅(hoisting)** 되어 선언이 코드의 최상단으로 이동한다. 하지만 **초기화는 선언 위치에서 이루어지기 때문에** 선언 전에 `x`를 출력하면 `undefined`가 출력된다.
    
    `let`으로 선언된 변수는 일시적 사각지대(TDZ)에 들어간다. 즉, `let` 선언 전에 해당 변수를 접근하려고 하면 `ReferenceError`가 발생한다.

    (출제위치: 15장 213쪽 첫번째 문단)
    </div>
    </details>
    <br>


1. 다음 코드를 보고 어떤 결과가 나올지 예측하고 설명하시오.
    
    ```jsx
    const numbers = [1, 2, 3];
    numbers.push(4);
    console.log(numbers);
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 코드는 정상작동한다. `numbers` 배열에 값 `4`가 추가됨

    `const`로 선언된 배열도 객체와 마찬가지로 내부 요소는 수정, 추가, 삭제가 가능하지만,
    배열 자체를 재할당할 수는 없다.
    
    (출제위치: 15장 217쪽 두번째 문단)
    </div>
    </details>
    <br>


1. 다음 코드를 보고 출력 결과를 예측하시오.
    
    ```jsx
    Object.defineProperty(person, 'lastName', {
      value: 'Lee'
    });
    
    descriptor = Object.getOwnPropertyDescriptor(person, 'lastName');
    console.log('lastName', descriptor);
    
    // 힌트: 데이터 프로퍼티 디스크립터 객체에는
    //      value, writable, enumerable, configurable 가 있다
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. `lastName {value: "Lee", writable: false, enumerable: false, configurable: false}`

    객체의 프로퍼티가 누락되었기 때문에 기본값인 `false` 로 설정되어 출력된다.
    디스크립터 객체의 프로퍼티를 누락시키면 `undefined`, `false`가 기본값이다.
    
    (출제위치: 16장 227쪽 예제 16-08)
    </div>
    </details>
    <br>


1. 객체를 재할당 없이 직접 변경하는 방법 세 가지를 제시하시오.
    
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    1. 프로퍼티를 추가하거나 삭제
    2. 프로퍼티의 값을 갱신
    3. `Object.defineProperty` 또는 `Object.defineProperties` 메소드를 사용하여
    프로퍼티 어트리뷰트를 재정의
    
    (출제위치: 16장 229쪽 첫번째 문단)
    </div>
    </details>
    <br>
    

    

2. 다음 코드를 보고, 생성자 함수에 의한 객체 생성 방식의 장점에 대해 논하시오.
    
    ```jsx
    const circle1 = {
      radius: 5,
      getDiameter() {
        return 2 * this.radius;
      }
    };
    
    console.log(circle1.getDiameter());
    
    const circle2 = {
      radius: 10,
      getDiameter() {
        return 2 * this.radius;
      }
    };
    
    console.log(circle2.getDiameter());
    
    /*****************************************************/
    
    function Circle(radius) {
      this.radius = radius;
      this.getDiameter = function () {
        return 2 * this.radius;
      };
    }
    
    const circle1 = new Circle(5);
    const circle2 = new Circle(10);
    
    console.log(circle1.getDiameter());
    console.log(circle2.getDiameter());
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 프로퍼티 구조가 동일한 객체 여러 개를 간편하게 생성할 수 있다.

    ```jsx
    const circle1 = {
      radius: 5,
      getDiameter() {
        return 2 * this.radius;
      }
    };
    
    console.log(circle1.getDiameter()); // 10
    
    const circle2 = {
      radius: 10,
      getDiameter() {
        return 2 * this.radius;
      }
    };
    
    console.log(circle2.getDiameter()); // 20
    
    /*****************************************************/
    
    // 생성자 함수
    function Circle(radius) {
      // 생성자 함수 내부의 this는 생성자 함수가 생성할 인스턴스를 가리킨다.
      this.radius = radius;
      this.getDiameter = function () {
        return 2 * this.radius;
      };
    }
    
    // 인스턴스의 생성
    const circle1 = new Circle(5);  // 반지름이 5인 Circle 객체를 생성
    const circle2 = new Circle(10); // 반지름이 10인 Circle 객체를 생성
    
    console.log(circle1.getDiameter()); // 10
    console.log(circle2.getDiameter()); // 20
    ```
    
    (출제위치: 14장 201쪽 다섯번째 문단)
    </div>
    </details>
    <br>
    

1. 다음 내용에 해당하는 빌트인 생성자 함수를 고르시오.
    
    ```
    (___A___, ___B___) 생성자 함수는 new 연산자 없이 호출해도 new 연산자와 함께 호출했을 때와
    동일하게 동작한다. 하지만, (__C__, ___D___, ___E___) 생성자 함수는 new 연산자와 함께
    호출했을 때 (__C__, ___D___, ___E___) 객체를 생성하여 반환하지만, new 연산자 없이 호출하면
    문자열, 숫자, 불리언 값을 반환한다. 이를 통해 데이터타입을 변환하기도 한다.
    ```
    
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 
    
    A: `Object`, B: `Function`, C: `String`, D: `Number`, E: `Boolean`

    (출제위치: 17장 248쪽 전체)
    </div>
    </details>
    <br>
