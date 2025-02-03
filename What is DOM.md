### **What is the DOM?**

The **DOM (Document Object Model)** is a programming interface for web pages. It represents the structure of an HTML document as a tree of objects, allowing JavaScript to dynamically interact with and manipulate web pages.

---

### **How the DOM Works**

- The **browser parses** an HTML document and creates a structured **DOM tree**.
- Each HTML element becomes a **node** in this tree.
- JavaScript can **read, modify, add, or remove elements** using the DOM API.

---

### **DOM Example**

#### **HTML Code**

```html
<!DOCTYPE html>
<html>
  <head><title>DOM Example</title></head>
  <body>
    <h1 id="title">Hello, DOM!</h1>
    <button onclick="changeText()">Click Me</button>

    <script>
      function changeText() {
        document.getElementById("title").innerText = "DOM Updated!";
      }
    </script>
  </body>
</html>
```

#### **How It Works**

- The **DOM** represents `<h1>` as an object in JavaScript.
- `document.getElementById("title")` finds the `<h1>` element.
- `.innerText = "DOM Updated!"` changes its content when the button is clicked.

---

### **DOM Tree Structure**

Example for:

```html
<div>
  <p>Hello</p>
  <p>World</p>
</div>
```

Would be structured as:

```
Document
 ├── <html>
 │   ├── <head>
 │   ├── <body>
 │       ├── <div>
 │           ├── <p> "Hello" </p>
 │           ├── <p> "World" </p>
```

---

### **Common DOM Methods**

|**Method**|**Description**|
|---|---|
|`document.getElementById(id)`|Selects an element by its ID.|
|`document.querySelector(css)`|Selects the first matching element.|
|`document.querySelectorAll(css)`|Selects all matching elements.|
|`element.innerHTML`|Gets/sets HTML inside an element.|
|`element.innerText`|Gets/sets text inside an element.|
|`element.style.property`|Modifies CSS styles.|
|`element.classList.add/remove/toggle`|Modifies CSS classes.|

---

### **Summary**

- The **DOM** represents an HTML document as a tree.
- JavaScript interacts with it using various methods.
- The DOM allows **dynamic changes** like updating content, styling, and handling events.