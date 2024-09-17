### 서술형 문제

1. 자바스크립트에서 변수를 선언할 때 '초기화'와 '선언' 단계가 어떤 의미인지 설명하고, 각각의 단계에서 자바스크립트 엔진이 수행하는 작업을 서술하시오.
   <details>
    <summary>01_answer</summary>
    <div markdown="1">
    A. 
        변수 선언 단계에서는 변수 이름이 자바스크립트 엔진에 등록되어 변수의 존재가 알림니다. 
        초기화 단계에서는 메모리 공간이 확보되고, 자바스크립트 엔진에 의해 자동으로 undefined가 변수에 할당됩니다. 
        이 단계는 변수 선언 후 첫 번째 값 할당을 의미합니다.
    </div>
    </details>
    
2. 변수 재할당의 개념을 설명하고, 변수가 어떻게 메모리에서 처리되는지 설명하시오. 또한, '가비지 콜렉터'가 어떻게 작동하는지 설명하시오.
   <details>
    <summary>02_answer</summary>
    <div markdown="1">
    A. 
        변수 재할당은 이미 값이 할당된 변수에 새로운 값을 다시 할당하는 것입니다. 
        이때, 자바스크립트 엔진은 새로운 메모리 공간을 확보하고 거기에 새로운 값을 저장합니다. 
        기존 값은 더 이상 참조되지 않으면 '가비지 콜렉터'에 의해 자동으로 메모리에서 해제됩니다. 
        가비지 콜렉터는 주기적으로 사용되지 않는 메모리 공간을 검사하여 해제함으로써 메모리 누수를 방지합니다.
    </div>
   </details>

### 객관식 문제

3. **다음 중 '변수 선언'의 올바른 설명은 무엇인가요?**
    - A) 변수 선언은 변수에 값을 할당하는 과정입니다.
    - B) 변수 선언은 메모리 공간을 확보하고 변수 이름과 메모리 주소를 연결합니다.
    - C) 변수 선언은 변수의 값을 읽는 과정입니다.
    - D) 변수 선언은 메모리에서 값을 제거하는 과정입니다.
   <details>
    <summary>03_answer</summary>
    <div markdown="1">
    A. 
        B
    </div>
   </details>
  
4. **다음 코드에서 `score` 변수의 값이 무엇으로 출력될까요?**
    
    ```jsx
    console.log(score);
    var score = 10;
    ```
    
    - A) 10
    - B) undefined
    - C) ReferenceError
    - D) null
   <details>
    <summary>04_answer</summary>
    <div markdown="1">
    A. 
        B
    </div>
   </details>
      
5. **변수 이름에 사용할 수 없는 것은 무엇인가요?**
    - A) _score
    - B) $amount
    - C) 2ndValue
    - D) firstName
   <details>
    <summary>05_answer</summary>
    <div markdown="1">
    A. 
        c
    </div>
   </details>
  
### OX 문제

6. 변수 호이스팅은 변수 선언문이 코드의 선두로 이동한 것처럼 동작한다. (O/X)
    <details>
    <summary>06_answer</summary>
    <div markdown="1">
    A. 
        O
    </div>
   </details>
    
7. 변수에 값을 재할당할 때, 기존 값은 새로운 값으로 덮어쓰여지며 기존 메모리 공간은 변경되지 않는다. (O/X)
   <details>
    <summary>07_answer</summary>
    <div markdown="1">
    A. 
        x (기존 값이 저장된 메모리 공간을 지우고 새로운 메모리 공간에 값을 저장합니다.)
    </div>
   </details>
    
8. 변수 선언 시, 변수 이름은 숫자로 시작할 수 있다. (O/X)
    <details>
    <summary>08_answer</summary>
    <div markdown="1">
    A. 
        x
    </div>
   </details>
