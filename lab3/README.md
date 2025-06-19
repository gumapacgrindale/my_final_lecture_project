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
