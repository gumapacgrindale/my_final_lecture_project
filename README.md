# My Final Lecture Project
Each folder contains:
- A `.java` source file for the activity.
- A `README.md` file that provides a comprehensive explanation of the code: what it does, what Java concepts are used, and how it works in practice.

📌 **For full explanations, please refer to the individual README.md files inside each folder, or see the summary at the end for compacted descriptions of each activity.**

---

## 📝 Summary of Each Activity

| Folder | Title | Focus |
|--------|-------|-------|
| `lab1` | Employee Info System (Part 1) | Input, Variables, Arithmetic |
| `lab2` | Employee Info System (Part 2) | Expanded Calculations, Math Functions |
| `lab3` | Conditional Version | `if`, `switch`, validation logic |
| `lab4` | GUI Version (AWT) | Layouts, Forms, TextFields, Buttons |
| `lab5` | Quiz App (AWT) | MCQ logic, arrays, radio buttons |
| `lab6` | To-Do List (Swing) | `JFrame`, `JTable`, Forms, Comboboxes |
| `labproject` | Final Project: Calculator | Operator precedence parser, `BigDecimal`, advanced math features |
| `midtermlabexam` | Midterm Exam Project | Ticket system with arrays, menu system, looping, validation |

---

## ▶️ How to Run the Activities

Each program can be compiled and run using **Java JDK** on your terminal or any Java IDE like **Eclipse**, **NetBeans**, or **IntelliJ**.

### 📦 For Console-based Programs (Lab 1-3, Midterm, Project):
1. Open your terminal or IDE.

2. Navigate to the folder (e.g., `cd lab1`)

3. Compile the Java file:
   ```bash
   javac LabActivity1EmployeeInformationSystem.java
   ```

4. Run the program:
  ```bash
  javac LabActivity1EmployeeInformationSystem.java
  ```

### 🖼️ For GUI-based Programs (Lab 4-6, Calculator):

1. Follow the same steps as above.

2. Make sure your screen allows pop-up windows (GUI will launch).

☑️ No external libraries required. All programs run using Java SE (Standard Edition).

## 🙋‍♂️ About This Repository
This compilation reflects my learning progress throughout the second semester in **Computer Programming 2 using Java**. It shows:
* My ability to work with both console-based and graphical user interface applications
* How I structure programs using methods, validation, arrays, loops, and OOP principles
* How I document and organize code professionally using Markdown

## 📢 PS: A Note from the Novice Developer (ME)
✨ I used `**ChatGPT by OpenAI**` to help me describe, document, and organize each activity in the best possible format. All code was written by me, and ChatGPT helped ensure that the explanations are well-structured, professional, and easy to understand for readers and evaluators.

##
Thank you for viewing my work! ⭐

— **Grindale Gumapac**

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

# Compacted Description
### 🧾 Lab Activity 1 Summary
This Java console application simulates a **basic employee information system**. It prompts the user to input their personal details and work hours, then calculates their **daily salary**.

### 🔑 Key Concepts:
- `Scanner` for user input
- Data types: `String`, `int`, `double`
- Basic arithmetic and salary computation
- `System.out.print` and `System.out.printf` for formatted output

### ⚙️ Process:

1. User inputs: name, age, hours worked, hourly wage

2. Program computes: `dailyWage = hoursWorked * hourlyWage`

3. Output: Full name, age, and daily salary in PHP (formatted)

### 🧪 Sample Output:
Displays formatted employee details and computed salary.

### 🔧 Real-World Use:
Useful for small payroll calculations, academic practice, or as a basic payroll component in larger systems.
#
### 🧾 Lab Activity 2 Summary
This program builds upon Lab 1 by adding **more detailed salary computations** and an estimate of **years left until retirement**. It calculates daily, weekly, monthly, gross yearly, and net yearly wages.

### 🔑 Key Concepts:
- Reuse of inputs: name, age, hours worked, hourly rate
- Math functions: `Math.abs()` and `Math.round()`
- Extended calculations (weekly × 5, monthly × 4, yearly × 12)
- Net salary computation with tax and fixed deduction

### ⚙️ Process:

1. User inputs: name, age, hours worked, hourly wage

2. Program calculates:

3. Years to retirement (65 - age)

4. Rounded daily salary

5. Weekly, monthly, and gross yearly salary

5. Net yearly salary: deducts 32% tax and PHP 1500 in benefits

6. Outputs all results in formatted PHP currency

### 🧪 Sample Output:
Displays full name (in uppercase), age, years to retirement, and a breakdown of all salary types.

### 🔧 Real-World Use:
Ideal for simulations of basic payroll systems that estimate yearly earnings and handle tax deductions.
#
### 🧾 Lab Activity 3 Summary
This program enhances the Employee Information System by introducing **input validation** and **role-based categorization** using **conditional statements** like `if-else` and `switch`.

### 🔑 Key Concepts:
- Input validation using if-else (e.g., age limits and hours worked restrictions)
- `return` used to exit the program early if invalid input is detected
- `switch` statement to map numeric role codes (1-4) to role names
- Extended salary calculations reused from previous labs

Tax logic with `if-else` based on income threshold

### ⚙️ Process:

1. User inputs: name, age, hours worked, hourly wage, and role code

2. Validates:
	- Age must be between 18 and 64
	- Hours worked must be between 1 and 24

3. Maps role code to position (e.g., 1 = Manager, 2 = Supervisor, etc.)

4. Calculates:
	- Daily, weekly, monthly, gross, and net yearly salary
	- Applies 32% tax if gross income > ₱250,000

5. Displays all info with formatted output

### 🧪 Sample Output:
Shows full name, position, age, years to retirement, and a detailed salary breakdown.

### 🔧 Real-World Use:
Simulates HR systems where inputs are validated and roles influence employment records. Introduces logic structure for filtering and controlling program flow.
#
### 🧾 Lab Activity 4 Summary
This lab upgrades the previous employee system into a **Graphical User Interface (GUI)** using Java **AWT (Abstract Window Toolkit)**. It allows users to input employee data via text fields and shows results in a text area.

### 🔑 Key Concepts:
- Java AWT GUI: Uses components like `Frame`, `Panel`, `Label`, `TextField`, `TextArea`, and `Button`
- Event Handling: `ActionListener` detects when the user clicks "Submit" and triggers computations
- Input validation: Ensures all form fields are filled and checks for correct data types (e.g., `Integer.parseInt()` and `Double.parseDouble()`)
- Dynamic GUI Output: Displays results in a non-editable text area after calculations

### ⚙️ Process:

1. GUI form collects:
	- First name, last name, age, hours worked, hourly rate

2. Validates:
- All fields are filled
- Age is a valid integer
- Hours and rate are valid numbers

3. Computes salary: `hours * rate`

4. Displays:
- Full name, age, and daily salary in formatted PHP output

### 🧪 Sample Output (GUI):

```
Full Name: Juan Dela Cruz
Age: 21 years old
Daily Salary: PHP 640.00
```	
### 🔧 Real-World Use:
Introduces form-based interfaces found in real business software. Demonstrates how GUI input/output works, foundational for inventory apps, POS systems, or HR tools.
#
### 🧾 Lab Activity 5 Summary
This activity demonstrates the creation of an interactive Quiz Application using Java AWT, where users answer multiple-choice questions through a GUI interface.

### 🔑 Key Concepts:
- GUI Components: Uses `Frame`, `Label`, `Checkbox`, `CheckboxGroup`, and `Button` to build an interactive quiz layout
- Event Handling: `ActionListener` processes user selections and manages navigation between questions
- Array Usage:
	- Stores questions, choices, and correct answers in arrays
	- Tracks current question index and score using static variables
- Dynamic UI Update:
	- Each time the user clicks "Next", the next question and choices are loaded dynamically
- Result Summary: Displays a final score after all questions are answered

### ⚙️ Process:

1. App loads and shows the **first question** with four multiple-choice answers

2. User selects an option and clicks **Next**

3. System checks if the answer is correct and updates the score

4. Moves to the next question or shows the final result after the last question

### 🧪 Sample Output (Final Result):
```
Quiz Completed! Your Score: 2 out of 3
```
### 🔧 Real-World Use:
Represents the logic used in e-learning systems, review centers, and online assessments. Combines user interaction with logical flow control, input validation, and result computation in a GUI environment.
#
### 🧾 Lab Activity 6 Summary
This lab showcases a **To-Do List Manager** built using **Java Swing**, demonstrating how to build **multi-window GUI applications** with dynamic data handling using tables.

### 🔑 Key Concepts:
- **Swing GUI**: Uses `JFrame`, `JPanel`, `JTable`, `JTextField`, `JTextArea`, `JComboBox`, and `JButton`
- **Table Management**: `JTable` and `DefaultTableModel` are used to store and display task records
- **Modular Windows**: Separates the viewer window and task form window using multiple `JFrame` instances
- **Form Validation**: Prevents submission of incomplete task details
- **Dynamic Table Update**: Each submitted task is added in real-time to the main viewer

### ⚙️ Process:

1. Viewer window opens with a button: **Add Task**

2. When clicked, it opens a form where the user fills in:
	- Task Name
	- Task Description
	- Task Status (from dropdown)

3. On clicking **Save Task**:
	- Input is validated
	- Task is added as a new row to the viewer’s task table
	- Form closes

### 🧪 Sample Output:
```
+----------------+---------------------------+-------------+
| Task Name      | Task Description          | Status      |
+----------------+---------------------------+-------------+
| Java Project   | Finish calculator module  | Ongoing     |
| Grocery List   | Buy eggs, milk, and rice  | Not Started |
+----------------+---------------------------+-------------+
```
### 🔧 Real-World Use:
Simulates core features of productivity apps like Trello, Notion, or task schedulers. Teaches the backbone of **data entry**, **GUI form handling**, and **visual record display**, essential in many business apps.
#
### 🧾 Final Lab Project Summary: Advanced Calculator
This project is a feature-rich calculator application built using Java Swing, showcasing advanced parsing, expression evaluation, and GUI design. It significantly expands beyond standard arithmetic, aiming for a real-world, precision-capable calculator experience.

### 🔑 Key Concepts & Features:
- Java Swing GUI:
	- Uses `JFrame`, `JTextField`, custom-styled `JButtons`, and `JPanel` for layout
	- Rounded buttons, clean UI, and dual-display (expression and result)
- BigDecimal Precision:
	- All calculations use `BigDecimal` for accurate handling of decimal numbers
- Expression Parsing:
	- Converts expressions into tokens using custom logic
	- Implements operator precedence (PEMDAS), exponentiation (^), percentage, and square root (√)

- Custom Evaluation Engine:
	- Parses and evaluates expressions using stacks
	- Handles unary operations (like `√`, `-`, `%`) and binary operations (`+`, `-`, `*`, `/`, `^`)
- Live Result Display:
	- While typing, the calculator shows the real-time computed result
- Clear (`C`) and Delete (`⌫`) Functionality

### 🔧 Real-World Use:
- Mimics the behavior of scientific calculators and calculator apps found on smartphones or desktops. This demonstrates knowledge in:
- GUI/UX design
- Mathematical expression handling
- Stack-based evaluation
- Real-time computing

### ⚠️ Limitations:
- No support for parentheses ()
- Doesn't handle malformed input robustly (e.g., 5++5)
- Doesn’t show detailed error messages (e.g., division by zero)
- Only supports a linear expression, no history or memory feature
#
### 🧾 Midterm Lab Exam Summary: IT Ticket System (Console-Based)
This special activity demonstrates a **ticketing system** where a user can manage support tickets using a **text-based menu**. It combines everything learned from previous labs — input/output, conditional logic, and salary-like record management — but adds **arrays and looping constructs** to support real-world functionality.

### 🔑 Key Concepts Used:
- Menu-Driven Program using `do-while` loop and `switch` statement
- Arrays to store multiple ticket entries (`String[][] ticketList`)
- Input Handling via `Scanner`
- Modular Methods: Separate functions for adding, updating, showing, and reporting tickets
- Looping and Validation to ensure clean data flow and logic

### 🧩 Ticket Structure:
- Each ticket stores:
- Issue Description
- Urgency Level (Low / Medium / High)
- Status (Default: Pending; updatable to In Progress or Resolved)

### 🔧 Real-World Use:
This mimics a basic help desk system, introducing:
- Record-based data handling (arrays)
- Updating entries with input validation
- Report generation logic

### ⚠️ Limitations:
- Maximum of 5 tickets only (due to static array)
- No persistent data (all input is lost after exit)
- No real-time filtering or sorting
- Input is not very robust (e.g., no trimming or retry loop on invalid input)

