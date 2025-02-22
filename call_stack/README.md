
# **Call Stack in JavaScript**

## **Overview**

The **Call Stack** is a data structure used by JavaScript to keep track of function calls. It follows a **Last In, First Out (LIFO)** order, meaning that the most recently added function is executed first.

### **How the Call Stack Works:**
1. When a function is called, it is added to the top of the stack.
2. When a function finishes executing, it is removed from the stack.
3. The program continues executing the next function on the stack.

### **Example:**

```js
function first() {
    console.log("First Function");
}

function second() {
    console.log("Second Function");
    first();
}

second();
```

### **Execution Flow:**
1. The `second()` function is called and added to the stack.
2. `second()` calls `first()`, which is added to the top of the stack.
3. `first()` executes and is removed from the stack.
4. `second()` executes and is removed from the stack.

---

## **Key Takeaways:**
- The **Call Stack** handles function execution and the order of calls.
- Functions are added to the stack when called and removed once executed.
- It helps manage the flow of code execution in JavaScript.

    