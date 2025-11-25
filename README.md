# 📉 Python Bisection Method Solver

A custom **Numerical Root Finder** implemented in Python. This program calculates the root of a non-linear equation using the **Bisection Method**. It utilizes the `numpy` library for mathematical operations and iteratively narrows down the interval until the root is found within a specific tolerance.

## 🚀 Features

* **Mathematical Function:** Currently configured to solve $f(x) = e^x - \sin(x)$.
* **Convergence Validation:** Uses the **Intermediate Value Theorem** to ensure a root exists between the user-provided points before starting ($f(a) \cdot f(b) < 0$).
* **Precision Control:** Finds roots with a high degree of accuracy (Tolerance set to $1 \times 10^{-7}$).
* **Safety Mechanisms:**
    * detects if no root exists in the selected interval.
    * Includes a maximum iteration counter (`n=100`) to prevent infinite loops.
* **Immediate Feedback:** Instantly reports the root and the number of iterations required.

## 🛠️ Algorithm Specifications

The solver uses the following parameters defined in the script:

| Category | Configuration in Code |
| :--- | :--- |
| **Target Function** | `np.exp(x) - np.sin(x)` |
| **Tolerance (`tol`)** | `1e-7` (0.0000001) |
| **Max Iterations** | `100` |
| **Midpoint Formula** | $c = \frac{a + b}{2}$ |
| **Stop Condition** | When `abs(f(c)) < tol` |

## 📂 Project Structure

The project consists of a single Python script that runs in the console:

1.  **`Bi-Section Method.py`**: Contains the function definition, logic loop, and user input handling.

## 💻 How to Run

### 1. Install Dependencies
This project requires **NumPy**. If you don't have it, install it via pip:

```bash
pip install numpy
```

### 2. Run the Script
Execute the python file in your terminal
```bash
Bi-Section Method.py
```

### 3. Input
The program will ask for two numbers (Num1 and Num2) that define the start and end of the interval
```text
Enter Num1: -5
Enter Num2: -1
```

## 📝 Generated Output

### Scenario 1: Successful Root Finding
Finding the root for $e^x - \sin(x)$ between -5 and -1.

#### Console Input
```text
Enter Num1: -5
Enter Num2: -1
```

#### Output
```text
Root found at x = -3.1830630 after 26 iterations
```

### Scenario 2: Invalid Interval 
If inputs are chosen where the function does not cross zero (e.g., between 0 and 1, where the function is positive at both ends)

#### Console Input
```text
Enter Num1: 0
Enter Num2: 1
```

#### Output
```text
Root found at x = -3.1830630 after 26 iterations
```

## ⚠️ Requirements
* **NumPy Library** (import numpy).
* **Python 3.x or above** 

 
