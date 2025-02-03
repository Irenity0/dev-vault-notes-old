
### **Object Methods in JavaScript**

An **object method** is a function that is stored as a property of an object. You define a method in an object to perform some behavior or actions related to that object.

#### **Creating Object Methods**:

You can define object methods in two ways:

1. **Using the `function` Keyword**:
    
    ```javascript
    let person = {
      name: "John",
      greet: function() {
        console.log("Hello, " + this.name);
      }
    };
    
    person.greet(); // "Hello, John"
    ```
    
2. **Using Shorthand Method Syntax** (ES6+):
    
    ```javascript
    let person = {
      name: "John",
      greet() {
        console.log("Hello, " + this.name);
      }
    };
    
    person.greet(); // "Hello, John"
    ```
    

#### **Key Points**:

- **`this`** inside the method refers to the object itself (in this case, the `person` object).
- You can call the method using dot notation (e.g., `person.greet()`).

#### **Example** with Multiple Methods:

```javascript
let car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2020,
  displayInfo() {
    return this.brand + " " + this.model + " " + this.year;
  },
  updateYear(newYear) {
    this.year = newYear;
  }
};

console.log(car.displayInfo()); // "Toyota Corolla 2020"
car.updateYear(2022);
console.log(car.displayInfo()); // "Toyota Corolla 2022"
```

#### **Using `this` in Methods**:

- **`this`** refers to the current object the method is part of. It allows the method to access the object's properties and methods.
- In the example above, `this.year` refers to the `year` property of the `car` object.

---

### **Summary**:

- **Object Methods**: Functions stored inside objects.
- **Syntax**: Can be created using `function` keyword or shorthand method syntax.
- **`this` Keyword**: Refers to the object the method belongs to, allowing access to its properties and other methods.