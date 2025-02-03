### Key ES6 Features:

1. **`let` and `const`**:
   - `let`: Declares block-scoped variables.
   - `const`: Declares block-scoped variables that cannot be reassigned.

Example:
```javascript
let x = 10;  // Can be reassigned
const y = 20;  // Cannot be reassigned
```

2. **Arrow Functions**:
   - Shorter syntax for functions, with automatic `this` binding.

Example:
```javascript
const add = (a, b) => a + b;
console.log(add(5, 3));  // Outputs: 8
```

3. **Template Literals**:
   - Use backticks (\``) for string interpolation and multiline strings.

Example:
```javascript
let name = "Alice";
console.log(`Hello, ${name}!`);  // Outputs: Hello, Alice!
```

4. **Default Parameters**:
   - Allows setting default values for function parameters.

Example:
```javascript
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}
greet();  // Outputs: Hello, Guest!
```

5. **Destructuring Assignment**:
   - Extract values from arrays or properties from objects into variables.

Example:
```javascript
// Array destructuring
let [a, b] = [1, 2];
console.log(a, b);  // Outputs: 1 2

// Object destructuring
const person = { name: "Alice", age: 25 };
const { name, age } = person;
console.log(name, age);  // Outputs: Alice 25
```

6. **Spread and Rest Operators**:
   - Spread (`...`): Expands an array or object.
   - Rest (`...`): Collects multiple elements into an array.

Example:
```javascript
// Spread in arrays
let arr1 = [1, 2];
let arr2 = [...arr1, 3, 4];  // [1, 2, 3, 4]

// Rest in functions
function sum(...numbers) {
  return numbers.reduce((a, b) => a + b);
}
console.log(sum(1, 2, 3));  // Outputs: 6
```

7. **Promises**:
   - For handling asynchronous operations like API calls.

Example:
```javascript
const fetchData = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Data fetched"), 2000);
});

fetchData.then(data => console.log(data));  // Outputs: Data fetched after 2 seconds
```

8. **Classes**:
   - A cleaner, more structured way to create objects and deal with inheritance.

Example:
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks.`);
  }
}

let dog = new Dog("Buddy");
dog.speak();  // Outputs: Buddy barks.
```

9. **Modules**:
   - ES6 introduced a module system that allows exporting and importing code between files.

Example:
```javascript
// file1.js
export const hello = () => "Hello, World!";

// file2.js
import { hello } from './file1.js';
console.log(hello());  // Outputs: Hello, World!
```
