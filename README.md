# Ex04 Simple Calculator - React Project
## Date: 26:5:26

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

### Calculator.js

```
import React, { useState } from "react";
import "./Calculator.css";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    if (value === "=") {
      try {
        setInput(eval(input).toString());
      } catch {
        setInput("Error");
      }
    } else if (value === "C") {
      setInput("");
    } else {
      setInput(input + value);
    }
  };

  const buttons = [
    "7",
    "8",
    "9",
    "/",
    "4",
    "5",
    "6",
    "*",
    "1",
    "2",
    "3",
    "-",
    "0",
    ".",
    "=",
    "+",
    "C",
  ];

  return (
    <div className="calculator">
      <h1>Simple Calculator</h1>

      <input
        type="text"
        value={input}
        className="display"
        readOnly
      />

      <div className="buttons">
        {buttons.map((btn, index) => (
          <button
            key={index}
            onClick={() => handleClick(btn)}
          >
            {btn}
          </button>
        ))}
      </div>
    </div>
  );
};

export default Calculator;
```
### Calculator.css

```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.calculator {
  width: 320px;
  background: white;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.2);
}

.calculator h1 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
}

.display {
  width: 100%;
  height: 60px;
  margin-bottom: 20px;
  text-align: right;
  font-size: 24px;
  padding: 10px;
  border: 2px solid #ddd;
  border-radius: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.buttons button {
  height: 60px;
  border: none;
  border-radius: 10px;
  background: #4f46e5;
  color: white;
  font-size: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.buttons button:hover {
  background: #4338ca;
}

.buttons button:active {
  transform: scale(0.95);
}

@media (max-width: 400px) {
  .calculator {
    width: 95%;
  }

  .buttons button {
    height: 50px;
    font-size: 18px;
  }
}
```
### App.js

```
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <Calculator />
    </div>
  );
}

export default App;
```

## OUTPUT

<img width="1897" height="904" alt="image" src="https://github.com/user-attachments/assets/a949a22e-16de-4c4f-85d1-b336994bb632" />
<br>
<img width="1912" height="907" alt="image" src="https://github.com/user-attachments/assets/8a65460e-fbdf-4d3e-b561-79efa2e7e7b3" />
<br>
<img width="1886" height="894" alt="image" src="https://github.com/user-attachments/assets/8cd4d4b8-2d75-43c5-95ea-177550ff4830" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
