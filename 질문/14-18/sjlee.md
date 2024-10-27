```jsx
var x = 1;
const bar = () => {var x = 10; foo();}
const foo = () => {console.log(x)};
bar(); // ?
foo(); // ?
```
scope는 함수 호출 방식에 따라 동적으로 결정된다. (O/X)

this는 함수 정의 방식에 따라 결정된다. (O/X)

```tsx
const parent = {
  species: 'human',
  greet() {
    return `Hello, I am a ${this.species}`;
  }
};

const child = Object.create(parent);
child.name = 'John';

console.log(child.name);     // (1)
console.log(child.species);  // (2)
console.log(child.hasOwnProperty('species')); // (3)

```

- 아래 출력은 어떻게 될까요?
    
    ```tsx
    function Animal() {
      this.type = 'Animal';
    }
    
    Animal.prototype.speak = function() {
      return 'I am an animal';
    };
    
    function Dog(name) {
      this.name = name;
    }
    
    Dog.prototype = Object.create(Animal.prototype);
    Dog.prototype.constructor = Dog;
    Dog.prototype.speak = function() {
      return `Woof! My name is ${this.name}`;
    };
    
    const dog = new Dog('Buddy');
    
    console.log(dog.speak());            // (1)
    console.log(dog.type);               // (2)
    console.log(dog.__proto__.__proto__.speak()); // (3)
    
    ```
    

- prototype과 __proto__의 차이는 무엇일까요?

```tsx
function Car(make, model) {
  this.make = make;
  this.model = model;
}

const myCar = new Car('Toyota', 'Corolla');

Car.prototype.year = 2020;

console.log(myCar.year); // (1)
myCar.year = 2021;
console.log(myCar.year); // (2)
delete myCar.year;
console.log(myCar.year); // (3)

```

- Object.prototype의 프로토타입은 null이다 (O/X)
