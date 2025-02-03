### **Immediately Invoked Function Expressions (IIFE) in JavaScript**

An **Immediately Invoked Function Expression (IIFE)** is a function that is defined and executed immediately after its creation. It’s a common pattern used to create a local scope in JavaScript, avoiding polluting the global scope.

#### **Syntax of an IIFE**:

```javascript
(function() {
  // Code inside the function
})();
```

- The function is wrapped in parentheses to turn it into an expression.
- The last pair of parentheses `()` invokes the function immediately.

Alternatively, you can use arrow functions:

```javascript
(() => {
  // Code inside the function
})();
```

#### **Example**:

```javascript
(function() {
  console.log("This is an IIFE!");
})();
```

- This will immediately print `"This is an IIFE!"` to the console as soon as it’s defined.

#### **Why Use IIFE?**

1. **Avoid Global Variables**: Variables declared inside an IIFE are not accessible outside, so they won’t pollute the global scope.
    
2. **Encapsulation**: It helps create a private scope for variables, preventing accidental overwriting of variables in the global scope.
    
3. **Modular Code**: IIFEs allow you to organize code into isolated blocks without interfering with other parts of the code.
    

#### **Example with Variables**:

```javascript
(function() {
  let privateVar = "I am private!";
  console.log(privateVar); // "I am private!"
})();

console.log(privateVar); // Error: privateVar is not defined
```

- `privateVar` is only accessible inside the IIFE and cannot be accessed from outside.

---

### **Summary**:

- **IIFE**: A function that is executed immediately after it is defined.
- **Use Cases**: Avoiding global scope pollution, creating private variables, and modularizing code.