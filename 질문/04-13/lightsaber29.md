1. 아래 코드의 실행 결과를 예측하고, 오류가 발생한다면 원인을 서술하시오.
    
    ```jsx
    let b = undefined;
    console.log(b.length);
    ```


2. 다음 코드를 보고 출력을 예상하시오.
    
    ```jsx
    let value;
    console.log(typeof value);
    
    value = null;
    console.log(typeof value);
    ```


3. 다음 코드를 보고 출력을 예상하시오.
    
    ```jsx
    ('b' + 'a' + + 'a' + 'a').toLowerCase()
    ```


4. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let value = "Hello";
    
    if (value) {
        console.log("참입니다.");
    } else {
        console.log("거짓입니다.");
    }
    ```


5. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let value = null;
    let result = value || "기본 값";
    console.log(result);
    ```


6. 다음 코드를 읽고 어떤 값이 출력될 지 예측하시오.
    
    ```jsx
    let a = 0;
    let b = 2;
    let result = a || b && 5;
    console.log(result);
    ```


7. 다음 코드를 보고 코드에 오류가 발생할 지 판단하고, 정상작동 한다면 출력을 예측하시오.
    
    ```jsx
    var foo = {
    	name: 'Lee',
    	name: 'Kim'
    }
    console.log(foo);
    ```


8. 다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    function changeValue(a) {
        a = 5;
    }
    
    let num = 10;
    changeValue(num);
    
    console.log(num);
    ```


9. 다음 코드를 보고 출력을 예측하시오.
    
    ```jsx
    let obj1 = { name: "subin" };
    let obj2 = obj1;
    
    obj2.name = "lightsaber29";
    
    console.log(obj1.name);
    console.log(obj2.name);
    ```


10. 다음 코드를 보고 출력을 예측하시오.
    
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


11. 다음 코드를 보고 출력을 예측하시오.
    
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
