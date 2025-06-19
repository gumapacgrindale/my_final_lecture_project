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

### Role Assignment via `switch`
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
