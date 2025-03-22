<h1 align="center">Session 2: Initial Steps in React! 🎉</h1>

![session 2](./repository-assets//session-2.jpg "session 2")

<p align="center">In this session, we’ll explore the foundational concepts needed to start building with React. We'll begin with an introduction to JavaScript ES6+ (ES2016) features that are essential for React development, Then, we’ll move on to setting up our first React app step by step. You'll find all the necessary links, commands, and resources in this section to guide you through the process smoothly. 🚀</p>

---

### Session Topics

- **[Revision Of JS(ES6)](#revision-of-js-es6)**

  - [VAR vs LET vs CONST](#var-vs-let-vs-const)
  - [JavaScript Destructuring](#javascript-destructuring)
  - [Spread Operator](#spread-operator)
  - [JavaScript-Object vs JSON-Object](#javascript-object-vs-json-object)
  - [Function Type](#function-type)

    - [Function Declaration](#function-declaration)
    - [Function Expression Anonymous](#function-expression-anonymous)
    - [Arrow Function (ES6)](#arrow-function-es6)

  - [Array Higher Order Functions](#array-higher-order-functions)

    - [map()](#map)
    - [filter()](#filter)
    - [forEach()](#foreach)

  - [Scope](#scope)

    - [Global-scope](#global-scope)
    - [Function-scope](#function-scope)
    - [Block-scope](#block-scope)

  - [Modules (import and export)](#modules-import-and-export)
  - [Logical and (&&) Operator and if else with Ternary Operators](#logical-and-operator-and-if-else-with-ternary-operators)

    - [Logical AND Operator](#logical-and-operator)
    - [Ternary Operator](#ternary-operator)

- **[React Requirements](#react-requirements)**

  - [Install Node.js](#install-nodejs)
  - [Make sure it is installed on your device.](#make-sure-it-is-installed-on-your-device)

- **[React Extension](#react-extension)**

  - [Browser Extension](#browser-extension)
  - [VS Code Extension](#vs-code-extension)

- **[Install React](#install-react)**

  - [React Official Website](#react-official-website)
  - [Install React](#install-react)

- **[💡 Client Task](#client-task)**

---

### Tools Used

<p>
    <a href="https://code.visualstudio.com/download">
        <img src="https://skillicons.dev/icons?i=vscode&perline=1" />
    </a>
</p>

---

### Revision Of JS (ES6)

<p>ES6 (ECMAScript 2015) is a major update to JavaScript that introduced many new features, making the language more powerful and easier to use.</p>

1.  #### VAR vs LET vs CONST

    1. ##### Hoisting

       Hoisting means that variable declarations are moved to the top of their scope during execution, but their initialization remains in place.

       ```bash
       console.log(a);
       var a = 10;
       ```

       ***

    2. ##### Reassignable

       This determines whether a variable can be assigned a new value after declaration.

       ```bash
       var x = 5;
       x = 10;
       console.log(x);
       ```

    ***

    3. ##### Redeclarable

       This determines whether a variable can be declared again in the same scope.

       ```bash
       var a = 10;
       var a = 20;
       console.log(a);
       ```

       ***

    | Feature        |    VAR    |      LET       |     CONST      |
    | -------------- | :-------: | :------------: | :------------: |
    | `Hoisting`     | undefined | ReferenceError | ReferenceError |
    | `Reassignable` |  ✅ Yes   |     ✅ Yes     |     ❌ No      |
    | `Redeclarable` |  ✅ Yes   |     ❌ No      |     ❌ No      |

> [!TIP]
> Exercise: [w3schools - Hoisting](https://www.w3schools.com/js/exercise.asp?x=xrcise_hoisting1) <br>
> Exercise: [w3schools - Let](https://www.w3schools.com/js/exercise.asp?x=xrcise_let1) <br>
> Exercise: [w3schools - Const](https://www.w3schools.com/js/exercise.asp?x=xrcise_const1)

---

2.  #### JavaScript Destructuring

      <p>The destructuring assignment syntax unpack object properties into variables</p>

    ```bash
    const fruits = ["Bananas", "Oranges", "Apples", "Mangos"];

    let [fruit1, fruit2] = fruits;

    console.log(fruits); // Output: ["Bananas", "Oranges", "Apples", "Mangos"]

    console.log(fruit1); // Output: Bananas

    console.log(fruit2); // Output: Oranges
    ```

> [!NOTE]
> When using array destructuring, you can skip values by leaving empty spaces separated by commas.

```bash
const numbers = [10, 20, 30, 40, 50];
const [first, , third] = numbers;

console.log(first, third); // Output: 10 30
```

> [!WARNING]  
> JavaScript destructuring work with ( Arrays, Objects, Strings ).

> [!TIP]
> Exercise: [w3schools - Destructuring](https://www.w3schools.com/js/exercise.asp?x=xrcise_destructuring1)

---

3.  #### Spread Operator

        <p>The JavaScript spread operator (...) allows us to quickly copy all or part of an existing array or object into another array or object.</p>

        ```bash
        const numbersOne = [1, 2, 3];
        const numbersTwo = [4, 5, 6];

        const numbersCombined = [...numbersOne, ...numbersTwo];

        console.log(numbersCombined ); // Output: [1, 2, 3,4, 5, 6]
        ```

> [!WARNING]  
> In JavaScript, the spread operator (...) works with ( Arrays, Objects, Strings ).

> [!TIP]
> Exercise: [w3schools - Spread Operator](https://www.w3schools.com/react/exercise.asp?x=xrcise_es6_spread1)

---

4.  #### JavaScript-Object vs JSON-Object

    | Feature       |        JavaScript-Object         |                             JSON-Object                              |
    | ------------- | :------------------------------: | :------------------------------------------------------------------: |
    | `Format`      |       In-memory structure        |                             Text format                              |
    | `Value-Types` | Can include functions, undefined | Only valid JSON types (string, number, boolean, array, object, null) |
    | `Usage`       |     Used in JavaScript code      |              Used for data exchange (e.g., APIs, files)              |

> [!TIP]
> Exercise: [w3schools - JavaScript Object](https://www.w3schools.com/js/exercise.asp?x=xrcise_objects1)<br>
> Exercise: [w3schools - JSON Object](https://www.w3schools.com/js/exercise.asp?x=xrcise_json1)

---

5.  #### Function Type

    1.  ##### Function Declaration

        ```bash
          function greet() {
            return "Hello!";
          }

          console.log(greet()); // "Hello!"
        ```

    ***

    2.  ##### Function Expression Anonymous

        ```bash
          const greet = function() {
            return "Hello!";
          };

          console.log(greet()); // "Hello!"
        ```

    ***

    3.  ##### Arrow Function (ES6)

        ```bash
          const greet = () => "Hello!";
          console.log(greet()); // "Hello!"
        ```

> [!TIP]
> Exercise: [w3schools - Function Declaration](https://www.w3schools.com/js/exercise.asp?x=xrcise_functions1)<br>
> Exercise: [w3schools - Arrow Function](https://www.w3schools.com/js/exercise.asp?x=xrcise_arrow_function1)

---

6.  #### Array Higher Order Functions

    1.  ##### map()

        A higher-order function that `creates a new array` by `applying a given function to each element of the original array`.

        ```bash
        const numbers = [1, 2, 3, 4, 5];

        const doubled = numbers.map(num => num * 2);

        console.log(doubled); // Output: [2, 4, 6, 8, 10]
        ```

    ***

    2.  ##### filter()

        A higher-order function that creates a `new array containing` only the elements `that satisfy a specified condition`.

        ```bash
        const numbers = [1, 2, 3, 4, 5];

        const evenNumbers = numbers.filter(num => num % 2 === 0);

        console.log(evenNumbers); // Output: [2, 4]

        ```

    ***

    3.  ##### forEach()

        A higher-order function that executes a function on each element of an array `without creating a new array.`

        ```bash
        const numbers = [1, 2, 3, 4, 5];

        numbers.forEach(num => console.log(num * 2));

        // Output:
        // 2
        // 4
        // 6
        // 8
        // 10
        ```

    ***

    | Function    | Returns New Array |
    | ----------- | :---------------: |
    | `map()`     |      ✅ Yes       |
    | `filter()`  |      ✅ Yes       |
    | `forEach()` |       ❌ No       |

---

7.  #### Scope

    <p>In JavaScript, scope refers to the accessibility of variables in different parts of the code. There are three main types of scope.</p>

    1.  ##### Global-scope

        A variable `declared outside any function or block`, making it accessible throughout the entire script.

        ```bash
        var globalVar = "I'm global";

        function example() {
          console.log(globalVar); // Accessible inside the function
        }

        example();
        console.log(globalVar); // Accessible anywhere
        ```

        ***

    2.  ##### Function-scope

        A variable `declared inside a function` making it accessible only within that function.

        ```bash
        function myFunction() {
          var functionVar = "I'm inside a function";
          console.log(functionVar);
        }

        myFunction();
        console.log(functionVar); // ❌ Error: functionVar is not defined
        ```

        ***

    3.  ##### Block-scope

        A variable `declared inside a block {}` making it accessible only within that specific block.

        1. ###### with ( var )

           ```bash
           if (true) {
             var testVar = "I'm declared with var";
           }

           console.log(testVar); // ✅ Accessible outside the block
           ```

        ***

        2. ###### with ( let/const )

           ```bash
           if (true) {
             let blockVar = "I'm inside a block";
             console.log(blockVar); // ✅ Accessible here
           }

           console.log(blockVar); // ❌ Error: blockVar is not defined
           ```

    ***

    | Scope Type     |  VAR   |  LET   | CONST  |
    | -------------- | :----: | :----: | :----: |
    | Global-scope   | ✅ Yes | ✅ Yes | ✅ Yes |
    | Function-scope | ✅ Yes | ✅ Yes | ✅ Yes |
    | Block-scope    | ❌ No  | ✅ Yes | ✅ Yes |

> [!TIP]
> Exercise: [w3schools - Scope](https://www.w3schools.com/js/exercise.asp?x=xrcise_scope1)

---

8.  #### Modules (import and export)

    <p>JavaScript modules are reusable pieces of code that are encapsulated and can be imported/exported between files. They help in organizing code better, improving maintainability, and preventing global scope pollution.</p>

    ```bash
    // math.js (Exporting module)
    export function add(a, b) {
        return a + b;
    }

    // main.js (Importing module)
    import { add } from './math.js';
    console.log(add(2, 3)); // Output: 5
    ```

---

9.  #### Logical and(&&) operator and if else with ternary operators

    1.  ##### Logical AND Operator

        ###### **Alternative to if**

        ```bash
        let isLoggedIn = true;

        isLoggedIn && console.log("Welcome back!");

        // Output: "Welcome back!"
        ```

    2.  ##### Ternary Operator

        ###### **Alternative to if-else**

        ```bash
        let age = 18;

        let status = "";
        if (age >= 18) {
          status = "Adult";
        } else {
            status = "Minor";
        }

        let status = age >= 18 ? "Adult" : "Minor";

        console.log(status); // "Adult"
        ```

### React Requirements

1. #### Install Node.js

   You must install Node.js to work with React effectively on a PC because React’s tools (like Create React App, Vite, and Next.js) depend on Node.js to manage packages, run the local server, and build the app.

    <p>
       <a href="https://nodejs.org/en/download">
           <img src="https://skillicons.dev/icons?i=nodejs&perline=1" />
       </a>
   </p>

---

2. #### Make sure it is installed on your device.

    <p>Type these commands inside the command prompt to get the current version of node.js</p>

   - current version of node.js

     ```bash
     node -v
     ```

   ***

   - current version of npm (Node Package Manager)
     ```bash
     npm -v
     ```

---

### React Extension

<p>Using a React extension in both the browser and VS Code can significantly improve your development experience.</p>

1. #### Browser Extension

   - [Install React Developer Tools](https://chromewebstore.google.com/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)

---

2. #### VS Code Extension

   - Integrates ESLint JavaScript into VS Code `ESLint`

   - Extensions for React, Redux in JS with babel and ES7 syntax `JS JSX Snippets`

   - Visual Studio Code plugin that autocompletes filenames `Path Intellisense`

   - Code formatter `Prettier - Code formatter`

   - Converts html code to React JSX `html to JSX`

> [!WARNING]
> Too many extensions can slow down VS Code or cause conflicts. It's best to keep only the essential ones and disable/uninstall the ones you don't use often.

---

### Install React

<p>Unfortunately, some libraries don't support the new React 19 release. This is a common issue when upgrading React versions. Therefore, I'll put you with two options. one to Install the latest version, and one to use it until the issue is resolved.</p>

1. #### React Official Website

   - [Old Official Website](https://legacy.reactjs.org/)
   - [New Official Website](https://react.dev/)

---

2. #### Install React

   - Install the latest version

     ```bash
     npx create-react-app <app name>
     ```

   ***

   - Install the version we will use in the course

     ```bash
     npx create-react-app@18.3.1 <app name>
     ```

<br>

---

<a id="client-task"></a>

### 💡 Client Task

```bash
Optimize Even Number Processing for a Math Learning App
Client: Sarah, Founder of "SmartMath", an educational platform for kids.

🎯 Project Brief:
Sarah wants a JavaScript function to help kids understand even numbers in an interactive way.

📌 The function should:
1️⃣ Filter even numbers from a given list.
2️⃣ Double each even number to make the learning experience more engaging.
3️⃣ Display the results on the webpage.
4️⃣ Allow new numbers to be added dynamically without modifying the original dataset.

📁 Resources
[5, 12, 7, 20, 15, 8, 10, 3]

This feature will be used in an interactive math exercise where kids can enter numbers and instantly see the transformed output.
```


### 💻 Solution

```bash
const numbers = [5, 12, 7, 20, 15, 8, 10, 3];

// 1️⃣ even numbers
const evenNumbers = numbers.filter(num => num % 2 === 0);

// 2️⃣ double each even number
const doubledNumbers = evenNumbers.map(num => num * 2);

// 3️⃣ display results in the console
doubledNumbers.forEach(num => console.log(num));

// 4️⃣ Add a new number dynamically
const updatedNumbers = [...numbers, 18];
console.log("\n Updated Number List:", updatedNumbers);
``` 

---

<div align="center">
<a href="#" >NEXT SESSION ></a>
</div>

---
