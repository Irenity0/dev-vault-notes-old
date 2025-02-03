### **What is `async/await`?**

`async/await` is a feature in JavaScript that simplifies writing and managing asynchronous code. It allows you to write asynchronous code in a way that looks and behaves like synchronous code, making it easier to read, write, and debug.

---

### **How Does `async/await` Work?**

1. **`async`**: Marks a function as asynchronous, allowing the use of `await` inside it. An `async` function always returns a **Promise**.
2. **`await`**: Pauses the execution of the `async` function until the Promise is resolved or rejected. It can only be used inside an `async` function.

---

### **Basic Syntax**

```javascript
async function fetchData() {
  const response = await fetch("https://api.example.com/data");
  const data = await response.json();
  console.log(data);
}

fetchData();
```

- **`async`**: Declares the `fetchData` function as asynchronous.
- **`await`**: Pauses the function until the `fetch` Promise resolves, then assigns the result to `response`.

---

### **Example: Without `async/await` (Using Promises)**

```javascript
function fetchData() {
  fetch("https://api.example.com/data")
    .then((response) => response.json())
    .then((data) => console.log(data))
    .catch((error) => console.error(error));
}

fetchData();
```

### **Same Code: With `async/await`**

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

fetchData();
```

- With `async/await`, the code looks cleaner and easier to follow.

---

### **Key Points**

1. **Error Handling**: Use `try...catch` blocks to handle errors in `async/await`.
2. **Sequential Execution**: `await` pauses execution, so tasks are performed sequentially.
3. **Parallel Execution**: Use `Promise.all` to run multiple `await` operations concurrently.

---

### **Example: Sequential vs. Parallel Execution**

#### Sequential

```javascript
async function sequential() {
  await asyncTask1();
  await asyncTask2();
  await asyncTask3();
}
```

#### Parallel

```javascript
async function parallel() {
  await Promise.all([asyncTask1(), asyncTask2(), asyncTask3()]);
}
```

---

### **Advantages of `async/await`**

- Improves code readability and reduces nesting.
- Easier to handle errors with `try...catch`.
- Works seamlessly with Promises.

---

### **Summary**

- `async/await` is built on top of Promises to simplify asynchronous programming.
- Use `async` to declare an asynchronous function and `await` to pause it until a Promise resolves.
- It makes asynchronous code easier to write and maintain.