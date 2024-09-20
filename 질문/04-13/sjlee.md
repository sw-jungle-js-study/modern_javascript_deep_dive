
## 05장 - 13장 문제
### 6장
<details>
<summary>Q1. ===과 == 연산자의 차이는 무엇인가요?</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q2. 아래의 출력값을 하나씩 말해주세요.
  
```javascript
'' == 0 // ?
null == false // ?
undefined == null // ?
NaN === NaN // ?
5 != '5' // ?
+0 === -0 // ?
Object.is(-0, +0) // ?
```

</summary>
<div markdown="1">
A.
</div>
</details>


### 8장
<details>
<summary>Q3. 아래의 출력값을 하나씩 말해주세요.

```javascript
var s1 = new String('hi');
var s2 = new String('hi');
s1 === s2; // ?
s1 == s2; // ?

// 논리곱 연산자
'Cat' && 'Dog' // ?
'Cat' || false // ?
false && 'Dog' // ?
```

</summary>
<div markdown="1">
</div>
</details>

### 10장
<details>
<summary>Q4. 자바스크립트에서 객체 프로퍼티 접근 방법을 아는대로 서술하세요.</summary>
<div markdown="1">
A. 
</div>
</details>

<details>
<summary>Q5. null의 typeof는 null을 반환하지 않고 object를 반환한다. 그럼 어떻게 null임을 확인할 수 있나?</summary>
<div markdown="1">
A. 
</div>
</details>

### 12장
<details>
<summary>Q6.function과 Arrow Function의 차이점은?
</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q7. addEventListener는 대표적인 콜백함수이다. btn이라는 id를 가진 버튼을 눌렀을때 "클릭됌"이라고 출력되는 함수를 만들어보세요.
</summary>
<div markdown="1">
A.
</div>
</details>

### 13장
<details>
<summary>Q8. 스코프 체인은 렉시컬 환경을 양방향으로 연결한 것이다. (O/X)
</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q9. 렉시컬 스코프는 어디서 호출되었는지에 따라 상위 스코프가 결정된다. (O/X)
</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q10. 아래의 출력값을 하나씩 말해주세요.

```javascript
var x = 1;
const bar = () => {var x = 10; foo();}
const foo = () => {console.log(x)};
bar(); // ?
foo(); // ?
```
  
</summary>
<div markdown="1">
A.
</div>
</details>


### 14장
<details>
<summary>Q11.객체의 불변성을 유지해야하는 이유는? 그리고 어떻게 불변성을 유지할 수 있는가?</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q12. 아래의 출력값을 말해주세요.

```javascript
const student = {
	name: 'SJLEE',
	address: { city: 'Seoul' },
}
Object.freeze(student);
student.address.city = 'Pohang';
console.log(student.address.city);
```
  
</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q13. 객체의 불변성을 유지할 수 있도록 깊은 복사를 하는 함수를 구현해주세요.
</summary>
<div markdown="1">
A.
</div>
</details>

### 15장
<details>
<summary>Q14. 함수 scope는 함수 호출 방식에 따라 동적으로 결정된다. (O/X)   
</summary>
<div markdown="1">
A. 
</div>
</details>

<details>
<summary>Q15. this는 함수 정의 방식에 따라 결정된다. (O/X)
</summary>
<div markdown="1">
A.
</div>
</details>

<details>
<summary>Q16. var 대신 let, const를 써야하는 이유를 말해주세요.
</summary>
<div markdown="1">
A.
</div>
</details>
