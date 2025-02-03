### **JavaScript Variables**

Variables are used to store data that can be referenced and manipulated later.

#### **Types of Variables**

1. **`var`**:
    
    - **Oldest way** to declare variables.
    - **Function-scoped**: Variables are limited to the function in which they are defined.
    - Can be **redeclared** and **updated**.
    - **Hoisted**: The declaration is moved to the top of its scope, but the assignment remains in place.
    
    ```javascript
    var name = "John";
    var name = "Doe"; // Redeclaring is allowed
    ```
    
2. **`let`**:
    
    - **Block-scoped**: The variable is limited to the block (e.g., within a loop, function, or condition) where it is defined.
    - Can be **updated** but **not redeclared** in the same scope.
    - **Hoisted**, but not initialized.
    - Introduced in ES6 (ES2015)
    
    ```javascript
    let age = 30;
    age = 31; // Allowed
    ```
    
3. **`const`**:
    
    - **Block-scoped**: Like `let`, but the value **cannot be reassigned** once it’s set.
    - Ideal for **constant values** or variables that should remain unchanged.
    - **Hoisted**, but must be initialized.
    - Introduced in ES6 (ES2015)
    
    ```javascript
    const pi = 3.14;
    pi = 3.1415; // Error: Assignment to constant variable.
    ```
    

---

### **Key Differences**:

- **Scope**:
    - `var`: Function-scoped.
    - `let`, `const`: Block-scoped.
- **Reassignment**:
    - `var` and `let`: Can be reassigned.
    - `const`: Cannot be reassigned.
- **Redeclaration**:
    - `var`: Can be redeclared.
    - `let` and `const`: Cannot be redeclared in the same scope.

### **Best Practice**:

- Use `let` for variables that might change.
- Use `const` for values that shouldn’t change.