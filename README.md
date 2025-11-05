# Ex04 Simple Calculator - React Project

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

## cal.JS

```
import React, { useState } from 'react';
import './index.css';

const Calculator = () => {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const calculate = () => {
    try {
      // eslint-disable-next-line no-eval
      setInput(eval(input).toString());
    } catch {
      setInput('Error');
    }
  };

  const clear = () => {
    setInput('');
  };

  return (
    <div className="calculator">
      <h2>Simple Calculator</h2>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {'1234567890+-*/.'.split('').map((char) => (
          <button key={char} onClick={() => handleClick(char)}>{char}</button>
        ))}
        <button onClick={calculate}>=</button>
        <button onClick={clear}>C</button>
      </div>
      <footer>
        <p>VIJAY K | Reg No: 212223040236</p>
      </footer>
    </div>
  );
};

export default Calculator;
```

## APP.js:

```
import React from 'react';
import Calculator from './Calculator';

function App() {
  return (
    <div className="App">
      <Calculator />
    </div>
  );
}

export default App;
```
## index.css
```
body {
  font-family: Arial, sans-serif;
  background-color: #fafafa;
  text-align: center;
}

.calculator {
  background: rgb(64, 217, 244);
  padding: 20px;
  margin: 50px auto;
  border-radius: 12px;
  max-width: 300px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

input {
  width: 100%;
  padding: 10px;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.buttons button {
  width: 60px;
  height: 40px;
  margin: 5px;
  font-size: 1.1rem;
  border: none;
  background: #0e08b6;
  color: white;
  border-radius: 5px;
}

footer {
  margin-top: 20px;
  font-size: 0.9rem;
  color: rgb(6, 4, 4);
}
```
## OUTPUT
![WhatsApp Image 2025-03-28 at 22 40 25_3a18970c](https://github.com/user-attachments/assets/2fe807bf-629e-4bde-91d5-233d120515c9)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
