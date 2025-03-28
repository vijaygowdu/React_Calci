# Ex04 Simple Calculator - React Project
## Date:28/03/2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

## APP.JS

```
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  function handleClick(value) {
    setInput(input + value);
  }

  function clearInput() {
    setInput("");
  }

  function calculateResult() {
    try {
      setInput(eval(input).toString()); 
    } catch (error) {
      setInput("Error");
    }
  }

  return (
    <div className="calculator">
      <h2>Calculator</h2>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {["7", "8", "9", "/", "4", "5", "6", "*", "1", "2", "3", "-", "0", ".", "=", "+"].map(function (char) {
          return (
            <button key={char} onClick={char === "=" ? calculateResult : function () { handleClick(char); }}>
              {char}
            </button>
          );
        })}
        <button className="clear" onClick={clearInput}>C</button>
      </div>
    </div>
  );
}

export default App;

```

## APP.CSS:

```

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #d78080;
  font-family: Arial, sans-serif;
}

.calculator {
  background: #e09e9e;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 250px;
}

h2 {
  margin-bottom: 10px;
}

input {
  width: 100%;
  height: 40px;
  text-align: right;
  font-size: 1.5em;
  padding: 5px;
  margin-bottom: 10px;
  border: 1px solid #e6d7d7;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
}

button {
  padding: 10px;
  font-size: 1.2em;
  background: #3498db;
  color: rgb(255, 255, 255);
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background: #2980b9;
}

.clear {
  grid-column: span 4;
  background: #e74c3c;
}

.clear:hover {
  background: #c0392b;
}


```

## OUTPUT

![image](https://github.com/user-attachments/assets/94ceed96-a463-4d25-9134-1c425df65da5)


![image](https://github.com/user-attachments/assets/6abf88f2-3948-45c7-b0fa-a6d51eb697b4)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
