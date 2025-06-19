# 🧾 Lab Activity 2: Employee Information System (Part 2)

## 📌 Description

This Java program is an enhanced version of the Employee Information System from Lab 1. In this version, the program not only calculates the **daily salary** but also computes the **weekly, monthly, gross yearly, and net yearly income** of an employee. It also estimates the number of **years left until retirement**, assuming retirement age is 65.

## 📂 File
- `LabActivity2EmployeeInformationSystemPart2.java`

## 🧠 Additional Concepts Used

This activity builds on Lab 1 and introduces the following **new concepts and calculations**:

1. **Math.abs()**
   - Used to compute the absolute value of the difference between the employee's age and the retirement age (65).
   - Example:  
     ```java
     int yearsToRetirement = Math.abs(65 - age);

2. **Rounding Numbers**
   - `Math.round()` is used to round the daily salary to the nearest whole number before further calculations.
   - Ensures that weekly, monthly, and yearly salaries are computed from a clean, whole number daily wage.

3. **Salary Calculations**
   - **Weekly Salary**: Daily wage × 5 (assuming 5 working days per week)  
   - **Monthly Salary**: Weekly wage × 4  
   - **Gross Yearly Salary**: Monthly wage × 12  
   - **Net Yearly Salary**: Deducts 32% tax and a ₱1,500 fixed deduction from the gross salary  
     ```java
     netYearlyWage = grossYearlyWage - (grossYearlyWage * 0.32) - 1500;

4. **String Formatting**
   - Names are displayed in uppercase using `toUpperCase()` for a more professional format.
   - Monetary values are formatted using `System.out.printf()` for 2 decimal places.

## 💻 How It Works (Step-by-Step

1. Prompts the user for:
   - First and last name
   - Age
   - Hours worked
   - Hourly wage

2. Performs calculations for:
   - Daily, weekly, monthly, gross yearly, and net yearly salaries
   - Years remaining before retirement

3. Displays all the computed data in a clean, professional layout.

## 🧪 Sample Output
```
Enter your first name: Grindale
Enter your last name: Gumapac
Enter your age: 23
Enter hours worked: 8
Enter hourly wage: 100

Employee Information
---------------------
Full Name:               GUMAPAC, GRINDALE  
Age:                     23 years old       
Years to Retirement:     42 years
Daily Salary:                     Php 800.00
Weekly Salary:                    Php 4000.00
Monthly Salary:                   Php 16000.00
Gross Yearly Salary:              Php 192000.00
Net Yearly Salary:                Php 129060.00
```

## 🔧 Practical Use

This extended version of the Employee Information System can serve as a **basic payroll simulator**, giving users a clearer understanding of their potential income across different periods and after taxes. It's a great way to demonstrate how arithmetic, formatting, and condition-based calculations work together in a real-world application.
