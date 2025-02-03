### **What is a Callback in JavaScript?**

A **callback** is a function that is passed as an argument to another function and is executed after the completion of that function. Callbacks are primarily used to handle asynchronous operations like API requests, file reading, or timers.

---

### **Why Use Callbacks?**

- **Asynchronous Programming**: JavaScript is single-threaded, so callbacks allow non-blocking execution while waiting for tasks like fetching data.
- **Reusability**: You can pass different callback functions to handle different scenarios.

---

### **How a Callback Works**

A function that takes another function as an argument is called a **higher-order function**. The function passed to it (the callback) is executed later.

#### **Example 1: Simple Callback**

```javascript
function greet(name, callback) {
  console.log("Hello, " + name);
  callback();
}

function sayGoodbye() {
  console.log("Goodbye!");
}

greet("John", sayGoodbye);
// Output:
// Hello, John
// Goodbye!
```

Here, `sayGoodbye` is the callback function passed to `greet`.

---

### **Callback with Asynchronous Operations**

#### **Example 2: Using Callbacks with `setTimeout`**

```javascript
function fetchData(callback) {
  setTimeout(() => {
    console.log("Data fetched");
    callback();
  }, 2000);
}

function processData() {
  console.log("Processing data...");
}

fetchData(processData);
// Output (after 2 seconds):
// Data fetched
// Processing data...
```

---

### **Callback Hell**

When multiple asynchronous operations rely on nested callbacks, it can lead to **callback hell**, making code hard to read and maintain.

#### **Example: Callback Hell**

```javascript
setTimeout(() => {
  console.log("Task 1");
  setTimeout(() => {
    console.log("Task 2");
    setTimeout(() => {
      console.log("Task 3");
    }, 1000);
  }, 1000);
}, 1000);
```

This is hard to read and debug, which is why **Promises** and **async/await** are now preferred alternatives.

---

### **Key Points**

- A **callback** is a function passed to another function to be executed later.
- Widely used for **asynchronous programming** in JavaScript.
- Can lead to **callback hell**, which is mitigated using Promises or `async/await`.