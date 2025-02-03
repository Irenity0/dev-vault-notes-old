### **DOM Manipulation in JavaScript**

DOM manipulation allows JavaScript to dynamically update the content, structure, and style of an HTML document.

---

### **Selecting Elements**

To manipulate elements, first, you need to select them.

|**Method**|**Description**|
|---|---|
|`document.getElementById(id)`|Selects an element by its ID.|
|`document.querySelector(css)`|Selects the first matching element.|
|`document.querySelectorAll(css)`|Selects all matching elements (NodeList).|
|`document.getElementsByClassName(class)`|Selects elements by class (HTMLCollection).|
|`document.getElementsByTagName(tag)`|Selects elements by tag name.|

#### **Example: Selecting Elements**

```javascript
const title = document.getElementById("main-title");
const buttons = document.querySelectorAll(".btn");
```

---

### **Changing Content & Attributes**

|**Method/Property**|**Description**|
|---|---|
|`element.innerHTML`|Gets or sets the HTML content inside an element.|
|`element.innerText` / `textContent`|Gets or sets only the text inside an element.|
|`element.setAttribute(attr, value)`|Sets an attribute (e.g., `src`, `href`).|
|`element.getAttribute(attr)`|Gets an attribute value.|
|`element.removeAttribute(attr)`|Removes an attribute.|

#### **Example: Changing Text & Attributes**

```javascript
title.innerText = "New Title!";
document.querySelector("img").setAttribute("src", "new-image.jpg");
```

---

### **Modifying Styles**

|**Method**|**Description**|
|---|---|
|`element.style.property`|Changes a specific CSS property.|
|`element.classList.add(class)`|Adds a CSS class.|
|`element.classList.remove(class)`|Removes a CSS class.|
|`element.classList.toggle(class)`|Toggles a CSS class on/off.|

#### **Example: Styling Elements**

```javascript
title.style.color = "red";
title.classList.add("highlight");
```

---

### **Adding & Removing Elements**

|**Method**|**Description**|
|---|---|
|`document.createElement(tag)`|Creates a new HTML element.|
|`parent.appendChild(child)`|Adds an element at the end of a parent.|
|`parent.insertBefore(new, ref)`|Inserts before a reference element.|
|`element.remove()`|Removes an element.|
|`parent.removeChild(child)`|Removes a child element.|

#### **Example: Creating and Removing Elements**

```javascript
const newPara = document.createElement("p");
newPara.innerText = "This is a new paragraph!";
document.body.appendChild(newPara); // Adds to body

newPara.remove(); // Removes the paragraph
```

---

### **Handling Events**

|**Method**|**Description**|
|---|---|
|`element.addEventListener(event, callback)`|Attaches an event listener.|
|`element.onclick = function`|Sets an event handler.|

#### **Example: Event Handling**

```javascript
document.querySelector(".btn").addEventListener("click", function () {
  alert("Button clicked!");
});
```

---

### **Summary**

- **Select elements** using `getElementById`, `querySelector`, etc.
- **Modify content** with `innerText`, `innerHTML`, and attributes.
- **Change styles** dynamically with `style` or `classList`.
- **Create, add, and remove elements** with `createElement`, `appendChild`, and `remove()`.
- **Handle user interactions** using event listeners.

This allows **dynamic web pages** with interactive content! 🚀