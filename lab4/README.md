# 🧾 Lab Activity 4: Employee Information System (GUI-Based)

## 📌 Description

This Java program demonstrates the Employee Information System using a **Graphical User Interface (GUI)**. It allows the user to input employee details and calculates the daily salary using Java AWT (Abstract Window Toolkit) components like `Frame`, `Panel`, `Label`, `TextField`, `Button`, and `TextArea`.

## 📂 File
- `LabActivity4EmpInfoSystemGUI.java`

## 🧠 New Concepts Used

This activity introduces a new approach using **AWT-based GUI programming** in Java, highlighting:

### 🖼️ Java AWT (Abstract Window Toolkit)

- **Frame**  
  The main application window that holds all components.
  ```java
  Frame frame = new Frame("Laboratory Activity 4");
  ```

- **Panel & Layouts**
  Used to organize components inside the frame.
  - `GridLayout` for form fields and outputs
  - `FlowLayout` for the submit button

    ```java
    Panel pnlForm = new Panel(new GridLayout(5, 2));
    ```

- **Labels, TextFields, and Button**
  UI components to accept and label inputs:
  ```java
  new Label("First Name");
  new TextField();
  new Button("Submit");
  ```

- **TextArea**
  Displays multiline output and error messages to the user.
  ```java
  TextArea taOutput = new TextArea(3,1);
  taOutput.setEditable(false);

### 🧩 Event Handling with `ActionListener`
- The `Submit` button triggers calculations using an **anonymous inner class**:
  
  ```java
  btnSubmit.addActionListener(new ActionListener() {
      public void actionPerformed(ActionEvent actEvent) {
          // logic here...
      }
  });
  ```

### 🧪 Input Validation
- Checks if all text fields are filled.
- Validates that:
  - Age is a valid integer
  - Hours worked and hourly rate are valid decimal numbers
- Uses `try-catch` blocks to handle invalid inputs gracefully and inform the user through the `TextArea`.

### 📊 Salary Calculation
- Once all inputs are validated, the daily salary is computed using:

  ```java
  double salary = hours * rate;
  ```
- The output is formatted using `String.format()` and displayed in the `TextArea`.

### 🛑 Graceful Exit Handling
- Uses `WindowAdapter` to close the window when the user clicks the “X” button:

  ```java
  frame.addWindowListener(new WindowAdapter() {
    public void windowClosing(WindowEvent winEvent) {
        frame.dispose();
      }
  });
  ```

## 💻 How It Works (Step-by-Step)

1. The user inputs their:
  - First name
  - Last name
  - Age
  - Hours worked
  - Hourly rate

2. When the Submit button is clicked:
  - The app validates all fields
  - Parses input values
  - Calculates the salary if inputs are valid
  - Displays results in the output box
  - Displays an error message if any input is invalid or missing

## 🧪 Sample Output
```
Full Name: Dale Gumapac
Age: 23 years old
Daily Salary: PHP 800.00
```

## 🔧 Practical Use
This GUI version provides a more user-friendly way to interact with applications. It simulates real-world desktop applications where users can:
- Enter data via forms
- See instant results without using the command line
- Get feedback if input is missing or incorrect

It’s a great introduction to event-driven programming and graphical interface design in Java.
