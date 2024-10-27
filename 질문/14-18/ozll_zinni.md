1. ( )안에 들어갈 말은?
    
    변수의 생명 주기는 메모리 공간이 (ㅤAㅤ)된 시점부터 메모리 공간이 (ㅤBㅤ)되어 (ㅤCㅤ)에 (ㅤDㅤ)되는 시점까지다
    <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    A : 확보
    B : 해제
    C : 메모리 풀
    D : 반환

    (출제위치: 14장)
    </div>
    </details>
    <br>

2. 캡슐화와 정보은닉에 대해 설명해주세요
   <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    캡슐화 : 객체의 데이터와 메서드를 하나의 단위로 묶는 것을 의미하며, 외부에서 직접 데이터에 접근하는 것을 방지하는 데 중점을 둡니다.
    정보 은닉 : 외부에서 불필요한 세부 구현을 숨기고, 클래스 내부의 데이터나 메서드를 외부로부터 보호하는 것

    (출제위치: 14장)
    </div>
    </details>
    <br>

    
4. 1️⃣,2️⃣번의 출력 결과와 이 코드의 부작용을 해결할 수 있는 방법을 찾은 후 그 후에 1️⃣,2️⃣ 출력 결과도 말씀하시오.
    
    ```
    function foo() {
      var x = 1;
    
      if (true) {
        var x = 2;
        console.log(x); // 1️⃣
      }
    
      console.log(x); // 2️⃣
    }
    
    foo();
    ```
    <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    - 수정 전 출력결과: 2,2
    - 부작용 해결 방법: var키워드를 let으로 변경한다
    - 수정 후 출력결과: 2,1

    (출제위치: 15장)
    </div>
    </details>
    <br>
        
5. 일시적 사각지대란 무엇일까요?
    <details>
    <summary>답</summary>
    <div markdown="1">
    A.

    스코프의 시작 지점부터 초기화 시작 지점까지 변수를 참조할 수 없는 구간을 일시적 사각지대(Temporal Dead Zone:TDZ)라고 부른다.

    (출제위치: 15장)
    </div>
    </details>
    <br>
6. 아래 출력 결과를 말씀하시오.
    
    ```
    const person = { age: 25 };
    Object.preventExtensions(person);
    
    console.log(Object.isExtensible(person)); // 1️⃣
    
    person.name = 'Lee';
    
    console.log(person); // 2️⃣
    
    Object.seal(person);
    
    console.log(Object.isSealed(person)); // 3️⃣
    
    delete person.age;
    
    console.log(person); // 4️⃣
    
    person.age = 100;
    
    console.log(person); // 5️⃣
    ```
    <details>
    <summary>답</summary>
    <div markdown="1">
        
    A.

    ```
    const person = { age: 25 };
    Object.preventExtensions(person);
    
    //Object.preventExtensions는 객체의 확장을 금지. 따라서 Object.isExtensible는 false를 반환.
    console.log(Object.isExtensible(person)); // 출력: false
    
    person.name = 'Lee';
    
    // 확장이 금지됐으므로 그대로 출력.
    console.log(person); // 출력: { age: 25 }
    
    Object.seal(person);
    
    //Object.seal은 객체의 프로퍼티 추가 및 삭제, 프로퍼티 어트리뷰트 재정의를 금지. 따라서 Object.isSealed는 true를 반환.
    console.log(Object.isSealed(person)); // 출력: true
    
    delete person.age;
    
    //delete person.age 금지된 동작이므로 age 프로퍼티가 삭제되지 않음.
    console.log(person); // 출력: { age: 25 }
    
    person.age = 100;
    
    //person.age = 100은 기존 프로퍼티 값을 갱신하려는 시도이므로, operson는 { age: 100 }으로 변경.
    console.log(person); // 출력: { age: 100 }
    ```
    (출제위치: 16장)
    </div>
    </details>
    <br>

7. 다음 설명 중 틀린 것을 모두 고르시오.
   ```
    1️⃣. 생성자 함수는 객체를 생성하기 위한 템플릿(클래스)으로 동작하여, 인스턴스를 생성하고 초기화하는 역할을 한다.
    2️⃣. 객체 리터럴에 의한 객체 생성 방식은 여러 개의 동일한 프로퍼티를 가진 객체를 효율적으로 생성할 수 있어 생성자 함수에 비해 유용하다.
    3️⃣. 생성자 함수를 호출할 때, 내부에서 사용되는 this는 생성될 인스턴스를 가리키며, 이를 통해 인스턴스를 초기화할 수 있다.
    4️⃣. 생성자 함수가 반환하는 값은 항상 생성된 인스턴스 자체이며, 다른 값을 반환하면 생성자 함수의 동작이 비정상적으로 이루어진다.
    5️⃣. 생성자 함수의 이름은 관례적으로 소문자로 시작하여야 하며, 이를 통해 일반 함수와 구별된다.
   ```
    <details>
    <summary>답</summary>
    <div markdown="1">
    A. 2️⃣, 5️⃣
      2️⃣: 객체 리터럴에 의한 객체 생성 방식은 효율적이지만, 여러 개의 동일한 프로퍼티를 가진 객체를 생성하는 데는 생성자 함수가 더 유용하다.
      
      5️⃣: 생성자 함수의 이름은 관례적으로 대문자로 시작하여야 하며, 이를 통해 일반 함수와 구별된다.

    (출제위치: 17장)
    </div>
    </details>
    <br>

8. 다음 설명 중 틀린 것을 고르시오.
```
  1️⃣. 함수는 무명의 리터럴로 생성할 수 있으며, 런타임에 생성이 가능하다.
  2️⃣. 함수는 변수나 자료 구조에 저장할 수 있으며, 객체에도 저장 가능하다.
  3️⃣. 함수는 매개변수로 전달할 수 없으며, 오로지 반환값으로만 사용할 수 있다.
  4️⃣. 함수 객체는 호출 가능하며, 함수 외에도 일반 객체와의 차이가 있다.
```
  <details>
  <summary>답</summary>
  <div markdown="1">
  A. 3️⃣ 함수는 매개변수로 전달할 수 있다.

  (출제위치: 18장)
  </div>
  </details>
  <br>

9. 다음 설명 중 틀린 것을 고르시오.
```
  1️⃣. 모든 객체는 내부 슬롯 [[prototype]]을 가지며, 객체 생성 시 프로토타입은 객체 생성 방식에 따라 결정되고 [[prototype]]에 저장된다.
  2️⃣. 프로토타입은 어떤 객체의 하위(자식) 객체가 상위(부모) 객체의 프로퍼티를 자유롭게 사용할 수 있도록 공유하는 역할을 한다.
  3️⃣. 프로토타입을 통해 생성된 객체는 자신의 `__proto__` 접근자 프로퍼티를 통해 프로토타입에 간접적으로 접근할 수 있다.
  4️⃣. `__proto__` 접근자 프로퍼티는 모든 객체가 직접 소유하는 프로퍼티로, 해당 객체의 프로토타입을 교체하는 데에 사용된다.
```
  <details>
  <summary>답</summary>
  <div markdown="1">
  A. 4️⃣
    모든 객체가 직접 소유하는 프로퍼티가 아니라 Object.prototype의 프로퍼티다.
    따라서 "모든 객체가 직접 소유하는 프로퍼티"라는 설명은 틀렸다.
    객체가 직접 소유하는 프로퍼티는 일반적으로 해당 객체의 프로퍼티들이며, __proto__는 이들 중 하나가 아니다.
  (출제위치: 19장)
    
  </div>
  </details>
  <br>
