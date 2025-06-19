# 🧾 Lab Activity 1: Employee Information System

## 📌 Description

This Java program simulates a simple **Employee Information System** where a user can input their personal and work-related details. The system then calculates and displays the **employee's daily salary** based on the input data.

## 📂 File
- `LabActivity1EmployeeInformationSystem.java`

## 🧠 Concepts Used

This activity demonstrates the following **fundamental Java concepts**:

1. **Importing Classes**  
   `import java.util.Scanner;` is used to enable user input through the console.

2. **Basic Input/Output**  
   The program uses `System.out.print` to prompt the user and `Scanner` methods (like `nextLine()`, `nextInt()`, and `nextDouble()`) to accept inputs such as name, age, hours worked, and hourly wage.

3. **Variables and Data Types**  
   - `String` for names  
   - `int` for age  
   - `double` for hours and wage

4. **Arithmetic Operations**  
   The program calculates the daily salary using the formula:  
   `dailyWage = hoursWorked * hourlyWage;`

5. **String Concatenation & Formatting**  
   - Combines user inputs to display full name  
   - Uses `System.out.printf()` for clean currency formatting (e.g., `PHP 480.00`)

## 💻 How It Works (Step-by-Step)

1. The user is prompted to enter:
   - First name
   - Last name
   - Age
   - Hours worked
   - Hourly wage

2. The program multiplies the hours worked by the hourly wage to calculate the daily salary.

3. Finally, it displays a formatted output showing:
   - The employee's full name
   - Age
   - Computed daily salary in PHP

## 🧪 Sample Output
```
Enter your first name: Grindale
Enter your last name: Gumapac
Enter your age: 19
Enter hours worked: 8
Enter hourly wage: 60

Employee Information
---------------------
Full Name   : Grindale Gumapac
Age         : 19 years old    
Daily Salary: PHP 480.00      
```
## 🔧 Practical Use

This kind of program can be used in:
- Small businesses to compute daily wages of employees
- Academic exercises to practice input handling and computations
- Larger systems as a foundational part of payroll features
