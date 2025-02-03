### **Event Listeners in JavaScript**

Event listeners allow you to listen for user interactions and execute a function when an event occurs.

---

### **`addEventListener()` Syntax**

```javascript
element.addEventListener(event, callback, useCapture);
```

- `event`: The event type (e.g., `"click"`, `"keydown"`).
- `callback`: Function to execute when the event occurs.
- `useCapture` (optional): `true` for capturing phase, `false` (default) for bubbling phase.

---

### **Example: Adding an Event Listener**

```javascript
document.getElementById("btn").addEventListener("click", function () {
  alert("Button clicked!");
});
```

---

### **Removing an Event Listener**

Use `removeEventListener()` to remove an event listener.

```javascript
function greet() {
  alert("Hello!");
}

const btn = document.getElementById("btn");
btn.addEventListener("click", greet);

// Remove listener
btn.removeEventListener("click", greet);
```

⚠️ **Important:** The function must be named (not anonymous) to remove it.

---

### **Event Object (`event`)**

The event object contains information about the event.

```javascript
document.addEventListener("click", function (event) {
  console.log("Event Type:", event.type);
  console.log("Clicked Element:", event.target);
});
```

---

### **Multiple Event Listeners**

```javascript
const btn = document.getElementById("btn");

btn.addEventListener("mouseover", () => console.log("Mouse Over"));
btn.addEventListener("click", () => console.log("Button Clicked"));
```

---

### **Event Delegation (Efficient Event Handling)**

Instead of adding event listeners to multiple elements, attach it to a parent element.

```javascript
document.getElementById("list").addEventListener("click", function (event) {
  if (event.target.tagName === "LI") {
    console.log("Clicked item:", event.target.textContent);
  }
});
```

✅ **Better Performance** for dynamic elements.

---

### **Common Event Types**

|**Event**|**Description**|
|---|---|
|`click`|When an element is clicked.|
|`dblclick`|Double-click event.|
|`keydown`|When a key is pressed.|
|`keyup`|When a key is released.|
|`mouseover`|When mouse enters an element.|
|`mouseout`|When mouse leaves an element.|

---

### **Summary**

- **Use `addEventListener()` to handle events.**
- **Use `removeEventListener()` to remove listeners.**
- **Event delegation improves performance.**
- **Use `event` object for more control.**

Mastering event listeners makes JavaScript **interactive & dynamic!** 🚀