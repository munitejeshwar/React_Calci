# Ex04 Simple Calculator - React Project
## Date:25/03/25
## Name: Muni Tejeshwar
## Reg. no: 212223040102
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
## App.css
```
.calculator {
  width: 250px;
  margin: 50px auto;
  padding: 20px;
  text-align: center;
  background: #222;
  color: white;
  border-radius: 10px;
}

input {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  text-align: right;
  font-size: 20px;
  padding: 5px;
  border: none;
  background: #333;
  color: white;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  background: #444;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background: #666;
}

.clear {
  grid-column: span 4;
  background: red;
}

```

## App.js
```
import React, { useState } from "react";
import "./App.css"; // For styling

function App() {
  const [input, setInput] = useState(""); // Store user input

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString()); // Evaluate the expression
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <h2>Simple Calculator</h2>
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {[7, 8, 9, "/", 4, 5, 6, "*", 1, 2, 3, "-", 0, ".", "=", "+"].map((char) => (
          <button
            key={char}
            onClick={() => (char === "=" ? calculateResult() : handleClick(char))}
          >
            {char}
          </button>
        ))}
        <button className="clear" onClick={clearInput}>
          C
        </button>
      </div>
    </div>
  );
}

export default App;


```
## OUTPUT

![image](https://github.com/user-attachments/assets/1babad3e-add6-4602-84e2-1e6db97e5962)

![image](https://github.com/user-attachments/assets/a7f8a611-5cdd-43fc-a45b-0b246c7cb851)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
