# Ex06 BMI Calculator
## Name : Ragavan E
## Reg NO : 212223040160

## AIM
To create a BMI calculator using React Router 

## ALGORITHM
### STEP 1 State Initialization
Manage the current page (Home or Calculator) using React Router.

### STEP 2 User Input
Accept weight and height inputs from the user.

### STEP 3 BMI Calculation
Calculate the BMI based on user input.

### STEP 4 Categorization
Classify the BMI result into categories (Underweight, Normal weight, Overweight, Obesity).

### STEP 5 Navigation
Navigate between pages using React Router.

## PROGRAM
## BMICalculator.jsx
```
import React, { useState } from 'react';
import './BMICalculator.css'; // Import the CSS file

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [result, setResult] = useState(null);
  const [error, setError] = useState('');

  const calculateBMI = () => {
    const w = parseFloat(weight);
    const h = parseFloat(height);
    
    if (!w || !h || isNaN(w) || isNaN(h) || w <= 0 || h <= 0) {
      setError('Please enter valid, positive numbers for both weight (kg) and height (cm).');
      setResult(null);
      return;
    }

    setError('');

    const heightInMeters = h / 100;
    const bmiValue = w / (heightInMeters * heightInMeters);

    const formattedBmi = bmiValue.toFixed(2);
    let message = '';

    if (bmiValue < 18.5) {
      message = 'You are **underweight**, gain some weight. 🙁';
    } else if (bmiValue >= 18.5 && bmiValue <= 24.9) {
      message = 'You have a **normal weight**. Great! 👍';
    } else if (bmiValue >= 25 && bmiValue <= 29.9) {
      message = 'You are **overweight**, reduce your weight. 😟';
    } else {
      message = 'You are **obese**, consider consulting a doctor. 🚨';
    }

    setResult({
      bmi: formattedBmi,
      message: message,
    });
  };

  // 
  return (
    <div className="bmi-container">
      <h1>BMI CALCULATOR</h1>
      <p>Enter your weight in kilograms and height in centimeters.</p>

      {/* Weight Input */}
      <div className="input-group">
        <label htmlFor="weight">Weight (kg):</label>
        <input
          id="weight"
          type="number"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
          placeholder="e.g., 70"
          min="1"
        />
      </div>

      {/* Height Input */}
      <div className="input-group">
        <label htmlFor="height">Height (cm):</label>
        <input
          id="height"
          type="number"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
          placeholder="e.g., 175"
          min="1"
        />
      </div>

      {/* Button to trigger calculation */}
      <button onClick={calculateBMI} className="bmi-button">
        Calculate BMI
      </button>

      {/* Display Error Message */}
      {error && <div className="bmi-error">{error}</div>}

      {/* Display Result */}
      {result && (
        <div className="bmi-result">
          <p>Your BMI is: <strong>{result.bmi}</strong></p>
          {/* Using dangerouslySetInnerHTML to render the bolded message */}
          <p dangerouslySetInnerHTML={{ __html: result.message }} />
        </div>
      )}
    </div>
  );
}

export default BMICalculator;
```
## BMICalculator.css
```
.App {
    
    min-height: 100vh; 
    width: 100vw; 
    display: flex;
    justify-content: center; 
    align-items: center; 
    
    margin: 0;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    
    background: linear-gradient(
        270deg,
        rgb(255, 0, 0),
        rgb(255, 165, 0),
        rgb(255, 255, 0),
        rgb(0, 128, 0),
        rgb(130, 0, 255),
        rgb(75, 0, 130),
        rgb(238, 130, 238)
    );
    background-size: cover; 
    background-position: center; 
    
    box-sizing: border-box; 
}

.bmi-container {
    background-color: whitesmoke;
    padding: 50px;
    border: 5px solid black;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5); /* Added shadow for pop */
    width: 90%;
    max-width: 450px;
}

.bmi-container h1 {
    color: white;
    background-color: rgb(16, 28, 193);
    padding: 10px;
    margin: -50px -50px 20px -50px;
    font-size: x-large;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
}
```
## App.jsx
```
import React from 'react';
import BMICalculator from './BMICalculator';

function App() {
  return (
    <div className="App">
      <BMICalculator />
    </div>
  );
}

export default App;
```


## OUTPUT


## RESULT
The program for creating BMI Calculator using React Router is executed successfully.
