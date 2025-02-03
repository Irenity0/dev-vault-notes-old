### **Hoisting in JavaScript**

**Hoisting** is a JavaScript behavior where variable and function declarations are moved (or "hoisted") to the top of their containing scope during the execution phase, before any code is run.

#### **Key Points about Hoisting**:

1. **Variable Hoisting (using `var`)**  
    Only the declaration (not the initialization) is hoisted. If you try to use a variable before it's initialized, you'll get `undefined`.
    
    ```javascript
    console.log(myVar); // undefined
    var myVar = "Hello";
    console.log(myVar); // "Hello"
    ```
    
    - `var myVar` is hoisted to the top, but the assignment (`= "Hello"`) is not.
2. **Function Hoisting**  
    Function declarations are hoisted completely. This means you can call a function before it’s declared in the code.
    
    ```javascript
    greet(); // "Hello, World!"
    
    function greet() {
      console.log("Hello, World!");
    }
    ```
    
3. **Hoisting with `let` and `const`**  
    Variables declared with `let` or `const` are hoisted, but they are not initialized until their declaration is encountered. If you try to access them before the declaration, you'll get a `ReferenceError` (known as the "temporal dead zone").
    
    ```javascript
    console.log(myVar); // ReferenceError: Cannot access 'myVar' before initialization
    let myVar = "Hello";
    ```
    
    - The declaration is hoisted, but accessing the variable before it's initialized causes an error.

#### **Summary**:

- **Hoisting**: JavaScript moves variable and function declarations to the top of their scope.
- **`var`**: Only the declaration is hoisted (not initialization).
- **Function Declarations**: Fully hoisted (can be called before declared).
- **`let` and `const`**: Hoisted but remain in the "temporal dead zone" until initialization.