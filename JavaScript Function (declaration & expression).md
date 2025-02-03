### **What is a JavaScript Function?**

A JavaScript function is a block of code that performs a specific task. You can define it once and call it whenever you need to run that task.

---

### **Function Declaration**

A function declaration defines a function using the `function` keyword. It's the most common way to create a function.

```javascript
function greet(name) {
  return "Hello, " + name;
}
```

You call it like this:

```javascript
greet("John"); // "Hello, John"
```

---

### **Function Expression**

A function expression defines a function and assigns it to a variable. It can be anonymous (without a name).

```javascript
const greet = function(name) {
  return "Hello, " + name;
};
```

You call it the same way:

```javascript
greet("John"); // "Hello, John"
```

---

### **Summary**:

- **Function Declaration**: `function` keyword, defined with a name.
- **Function Expression**: Assigned to a variable, can be anonymous.