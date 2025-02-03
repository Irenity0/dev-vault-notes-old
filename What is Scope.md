**Scope** refers to the context in which variables are accessible or visible. It determines where variables, functions, and objects can be accessed within your code.

#### **Types of Scope**

1. **Global Scope**  
    Variables declared outside of any function or block are in the global scope. They are accessible throughout the entire script.
```js
let person = {
  name: "John",
  greet: function() {
    console.log("Hello, " + this.name);
  }
};

person.greet(); // "Hello, John"
```

2. **Local Scope**  
    Variables declared inside a function are in the **local scope** of that function. They are only accessible within that function.

```js
function example() {
  let localVar = "I am local";
  console.log(localVar); // "I am local"
}

example();
console.log(localVar); // Error: localVar is not defined

```

  
3. **Block Scope (ES6)**  
    Variables declared using `let` or `const` inside a block (e.g., `if`, `for`) are in **block scope** and are only accessible within that block.

```js
if (true) {
  let blockVar = "I am in a block";
  console.log(blockVar); // "I am in a block"
}

console.log(blockVar); // Error: blockVar is not defined

```

4. **Function Scope**  
    Variables declared inside a function are limited to that function’s scope, meaning they are only accessible inside the function.

```js
function myFunction() {
  let myVar = "Hello!";
  console.log(myVar); // "Hello!"
}

console.log(myVar); // Error: myVar is not defined

```

---

### **Summary**:

- **Global Scope**: Variables accessible anywhere in the code.
- **Local Scope**: Variables accessible only within the function they are defined.
- **Block Scope**: Variables accessible only within the block (using `let` or `const`).
- **Function Scope**: Variables are only accessible inside the function they are declared in.