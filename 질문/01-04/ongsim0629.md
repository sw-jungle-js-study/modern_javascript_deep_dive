# OX 문제
#### 1. 자바스크립트는 브라우저에서만 동작한다. ( )
<details>
   <summary>답</summary>
   <div markdown="1">
      X, Node.js는 자바스크립트 엔진을 브라우저에서 독립시킨 자바스크립트 실행환경이다.
   </div>
</details>

<details>
   <summary> 꼬리 질문 </summary>
   <div markdown="1">
      Node.js 와 브라우저는 용도가 다릅니다. 어떻게 다를까요?
      <details>
         <summary>답</summary>
            <div markdown="1">
               브라우저 : 웹페이지를 브라우저 화면에 렌더링하는 것이 주된 목적, Node.js는 브라우저 외부에서 자바스크립트 실행 환경을 제공하는 것이 목적.
            </div>
      </details>
   </div>
   <div markdown="1">
     그러면 이러한 특징을 생각하면 DOM API를 제공하는 것은 브라우저일까요 Node.js일까요?
      <details>
         <summary>답</summary>
            <div markdown="1">
               브라우저
            </div>
      </details>
   </div>
      <div markdown="1">
     그러면 파일 시스템을 제공하는 것은 브라우저일까요 Node.js일까요?
      <details>
         <summary>답</summary>
            <div markdown="1">
               Node.js
            </div>
      </details>
   </div>
</details>

#### 2. 자바스크립트는 개발자의 직접적인 메모리제어를 허용하지않는다. ( )
<details>
   <summary>답</summary>
   <div markdown="1">
      O
   </div>
</details>

#### 3. var 키워드로 선언한 변수는 값을 재할당할 수 없다. (  )
<details>
   <summary>답</summary>
   <div markdown="1">
       X, 재할당할 수 있다. const는 재할당할 수 없다!
   </div>
</details>

# 빈칸 채우기
#### 1. 웹 페이지 또는 웹 애플리케이션이 다양한 브라우저와 버전에서 개발자의 의도대로 올바르게(호환성) 작동하지 않는 문제를 (  ) 이슈라고 한다.
<details>
   <summary>답</summary>
   <div markdown="1">
       크로스 브라우징
   </div>
</details>

#### 2. var 키워드를 이용해서 변수를 선언하면 자바스크립트 엔진은 암묵적으로 ( )를 할당해서 변수를 초기화한다.
<details>
   <summary>답</summary>
   <div markdown="1">
       undefined 
   </div>
</details>

<details>
   <summary> 꼬리 질문 </summary>
   <div markdown="1">
      그렇다면 let, const를 이용해서 변수로 선언을 할 때도 var 키워드를 이용할 때와 똑같이 변수가 ( undefined )로 초기화 될까요?
      <details>
         <summary>답</summary>
            <div markdown="1">
                No
            </div>
      </details>
   </div>
   <div markdown="1">
     그렇다면 let, const를 이용해서 선언된 변수들도 호이스팅 될까요?
      <details>
         <summary>답</summary>
            <div markdown="1">
               Yes, 호이스팅되지만 초기화되기 전에는 TDZ(Temporal Dead Zone, 일시적 사각지대)라고 불리는 곳에 완전히 초기화되지 않은 상태로 놓여서 접근할 수 없다. 그래서 초기화 전의 변수에 접근하려고 하면 ReferenceError (정의되지 않은 변수나 객체를 참조하려고 할 때 발생하는 오류)가 발생하게 된다. 
            </div>
      </details>
</details>

# 서술형
#### 1. 비동기의 의미를 서술하세요.
<details>
   <summary>답</summary>
   <div markdown="1">
      비동기는 '병렬적'으로 작동하는 방식으로 특정 코드가 끝날때 까지 코드의 실행을 멈추지 않고 다음 코드를 먼저 실행하는 것을 의미한다.
      js는 싱글 스레드여서 순차적으로 실행하지만, 동시에 다른 작업을 할 수 있는 것이다 => promise, async, await, call back
   </div>
</details>

#### 2. 변수 호이스팅에 대해서 설명하세요.
<details>
   <summary>답</summary>
   <div markdown="1">
      변수 선언이 실제 코드 실행 전에 해당 스코프의 최상단으로 끌어올려지는 것처럼 동작하는 메커니즘
   </div>
</details>

# 객관식
#### 자바스크립트의 특징이 아닌 것을 고르세요
① 개발자가 별도의 컴파일 작업을 수행하지 않는 컴파일러 언어이다.<br>
② 명령형, 함수형, 프로토타입 기반 객체지향 프로그래밍을 지원하는 멀티 패러다임 프로그래밍 언어이다.<br>
③ 프로토타입 기반의 객체지향 언어이다.<br>
④ 웹 브라우저에서 동작하는 유일한 프로그래밍 언어이다. <br>
<details>
   <summary>답</summary>
   <div markdown="1">
       ① 자바스크립트는 코드가 실행되는 단계인 런타임에 문 단위로 한 줄씩 코드를 변환하고 실행하는 인터프리터 언어이다.
   </div>
</details>
