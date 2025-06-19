# 🧾 Lab Activity 3: Employee Information System (Conditional Statements)

## 📌 Description

This Java program expands the Employee Information System from previous labs by integrating **conditional logic** and **data validation** using `if`, `else`, and `switch` statements. It simulates a more realistic employee entry system that restricts invalid entries, rejects inputs for minors or senior citizens, and assigns role descriptions based on input codes.

## 📂 File
- `LabActivity3ConditionalStatement.java`

## 🧠 Additional Concepts Used

This activity introduces the following **new Java concepts and practical implementations**:

### ✅ Input Validation with Conditional Statements

- **Age Restriction**  
  Prevents users younger than 18 and older than or equal to 65 from proceeding. Uses `if-else` with a ternary operator for custom messages:
  ```java
  if (age < 18 || age >= 65) {
      validationMessage = (age < 18) ? "Minors are not allowed" : "Senior Citizens are not allowed";
      return;
  }
  ```

- **Work Hour Limit**
  Validates that work hours do not exceed 24 and are greater than 0:
  ```java
  if (hoursWorked > 24 || hoursWorked <= 0) {
      // Rejects invalid input
      return;
  }
  ```

### 🔄 Role Assignment via `switch`
- Accepts numeric input (1–4) and assigns a corresponding role name (e.g., Manager, Supervisor, etc.).
- Demonstrates usage of the `switch` statement for decision branching:
  ```java
  switch (roleCodeNumber) {
    case 1: roleCodeName = "Manager"; break;
    case 2: roleCodeName = "Supervisor"; break;
    case 3: roleCodeName = "Staff"; break;
    case 4: roleCodeName = "Intern"; break;
    default: roleCodeName = "Undefined";
  }
  ```

### 💸 Conditional Tax Deduction
- Introduces **conditional tax calculation**:
  - If gross yearly salary exceeds ₱250,000, a 32% tax is applied.
  - Otherwise, no tax is deducted.
  ```java
  if (grossYearlyWage > 250000) {
    tax = grossYearlyWage * 0.32;
  } else {
      tax = 0;
  }
  ```

## 💻 How It Works (Step-by-Step)

1. Accepts user input for personal info, hours worked, wage, and role code.

2. Validates:
    - Age: Must be 18 to 64.
    - Work hours: Must be between 1 and 24.

3. Uses a switch to determine the job title.

4. Calculates various salary metrics: daily, weekly, monthly, gross yearly, and net yearly.

5. Applies tax only if salary exceeds a defined threshold.

6. Displays all results in an organized and professional format.

## 🧪 Sample Output
```
Enter your first name: Grindale
Enter your last name: Gumapac
Enter your age: 23
Enter hours worked: 8
Enter hourly wage: 100
Enter role code (1-Manager, 2-Supervisor, 3-Staff, 4-Intern): 2

Employee Information
---------------------
Full Name:              GUMAPAC, GRINDALE
Age:                    23 years old
Position:               Supervisor
Years to Retirement:    42 years
Daily Salary:           Php 800.00
Weekly Salary:          Php 4000.00
Monthly Salary:         Php 16000.00
Gross Yearly Salary:    Php 192000.00
Net Yearly Salary:      Php 189500.00
```

## 🔧 Practical Use
This upgraded version demonstrates basic decision-making logic required in real-world applications like:
- Employee management systems
- HR validation tools
- Financial calculators with conditional logic
