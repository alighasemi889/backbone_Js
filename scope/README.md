
# **Scope in JavaScript**

## **Overview**

In JavaScript, **scope** refers to the context in which a variable is declared and accessible. It defines the visibility of variables in different parts of your code.

### **Types of Scope:**
1. **Global Scope**: Variables declared outside any function are in the global scope and accessible anywhere.
2. **Local Scope**: Variables declared inside a function are only accessible within that function.
3. **Block Scope**: Variables declared using `let` or `const` inside a block (like loops or conditionals) are only accessible within that block.

### **Example:**

```js
let globalVar = "I am global";

function test() {
    let localVar = "I am local";
    console.log(globalVar); // Accessible
    console.log(localVar);  // Accessible
}

test();

console.log(localVar);  // Error: localVar is not defined
```

### **Execution Flow:**
1. `globalVar` is accessible throughout the code.
2. `localVar` is only accessible inside the `test()` function.
3. Attempting to access `localVar` outside the function results in an error.

---

## **Key Takeaways:**
- **Global Scope**: Variables are accessible everywhere.
- **Local Scope**: Variables are only accessible inside the function they are declared in.
- **Block Scope**: Variables declared with `let` or `const` are only accessible within the block.

    