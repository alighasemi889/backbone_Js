# backbone_Js



# **Execution Context in JavaScript**


![mFQtgsb](https://github.com/user-attachments/assets/79b37740-7760-4d9f-afab-9b2feaea68ef)

## **Overview**

In JavaScript, **Execution Context** refers to the environment where the code is evaluated and executed. It defines the rules for variable and function lookups, and how the execution stack operates.

### **Types of Execution Context:**
1. **Global Execution Context (GEC)**
2. **Function Execution Context (FEC)**

---

## **1. Global Execution Context (GEC)**

- The first Execution Context created when the program starts executing.
- It remains in the **Call Stack** until the program finishes executing.
- The **Global Context** includes the **global object** (`window` in the browser) and any global variables.

### Key Points:
- It’s created once when the program begins.
- Remains throughout the execution.
  
---

## **2. Function Execution Context (FEC)**

- Every time a function is called, a new **FEC** is created and pushed to the **Call Stack**.
- After the function finishes executing, its **FEC** is popped off the stack.
  
### Key Points:
- Created each time a function is invoked.
- It contains information like local variables and function arguments.

---

## **Execution Process:**

### **Steps of Execution in JavaScript:**
1. **Global Execution Context (GEC)** is created and added to the **Call Stack**.
2. When a function is called, a new **Function Execution Context (FEC)** is created and pushed onto the stack.
3. After the function finishes executing, the **FEC** is removed from the stack, but the **GEC** remains until the program completes.

---

## **Example:**

```js
function a() {
    function b() {
        console.log("Hello from B!");
    }
    b();
}

a();
```

### **Execution Flow:**
1. **GEC** is created and pushed to the Call Stack.
2. The function `a()` is called, creating an **FEC for `a`**.
3. Inside `a()`, function `b()` is called, creating an **FEC for `b`**.
4. `console.log("Hello from B!")` is executed.
5. **FEC for `b`** is removed from the stack.
6. **FEC for `a`** is removed from the stack.
7. **GEC** remains on the stack.

---

## **Key Takeaways:**
- **Global Execution Context (GEC)**: The first context that remains throughout the program execution.
- **Function Execution Context (FEC)**: Created when a function is called, and removed after the function finishes execution.
- The **Call Stack** helps manage which Execution Context is currently running.

---

### **Summary:**
The **Global Execution Context** is created once and stays until the program ends. However, for every function call, a new **Function Execution Context** is created and removed once that function finishes executing. The **Call Stack** is essential in managing these contexts as the program runs.
