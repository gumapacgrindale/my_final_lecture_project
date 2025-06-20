# 🧮 Final Lab Project: Advanced Calculator (Java Swing)

## 📌 Description

This is a feature-rich calculator application developed using **Java Swing**. It provides a visually appealing GUI interface and supports both basic and advanced arithmetic operations. The calculator is designed to handle input precision and common usability patterns, simulating the behavior of real-world and desktop calculators.

This lab project showcases the integration of GUI components, expression parsing, precision handling, and responsive design in Java.

## 📂 File
- `FinalLabProjectCalculator.java`

## ✨ Features

This calculator application includes the following capabilities:

| Feature | Description |
|--------|-------------|
| 🧮 **Basic Operations** | Addition (+), Subtraction (−), Multiplication (×), Division (÷) |
| 📐 **Advanced Math** | Square Root (√), Exponentiation (^), Percentage (%) |
| 🆎 **Sign Toggle** | Change between positive/negative values (+/-) |
| 💠 **Decimal Handling** | Proper formatting and input of decimal numbers |
| ⌫ **Backspace** | Delete the last character entered |
| 🧹 **Clear** | Reset both input and result fields (`C` button) |
| ✅ **Real-Time Expression Display** | Shows the current mathematical expression being built |
| 🧠 **BigDecimal Precision** | Ensures high-precision calculations and avoids floating-point issues |
| 👁️‍🗨️ **Responsive Input Validation** | Prevents invalid entries like consecutive operators or multiple decimal points |
| 🎨 **Custom Theming** | Clean visual layout with custom color palette and rounded button design |

## 🧠 Java Concepts Used

This project applies several core and advanced Java concepts:

### 🖼️ Java Swing GUI
- `JFrame`, `JPanel`, `JTextField`, `JButton`, `GridBagLayout` for creating a modern and resizable calculator window.

### 🧮 BigDecimal for Precision
- `BigDecimal` is used instead of primitive `double` to prevent floating-point errors and manage accurate financial or scientific calculations.

  ```java
  BigDecimal num1 = new BigDecimal("123.45");
  BigDecimal num2 = new BigDecimal("67.89");
  BigDecimal result = num1.add(num2);

### 🎛️ Event-Driven Programming
- Implements `ActionListener` to handle user interactions with buttons, including input parsing and expression evaluation.

### 💡 Custom Parsing Logic
- Parses string-based expressions to compute operations following proper operator precedence (e.g., `^`, `√`, `%` before basic operations).
- Includes support for unary operators (e.g., negative values).

### 🧩 Layout Management
- Uses `GridBagLayout` and responsive sizing to control the position and alignment of buttons and display panels.

### ⏱️ Timer for Feedback (Optional Flash Effect)
- `Timer` was prepared (though may be unused or optional) to add visual feedback like flashing buttons for interaction enhancement.

### 🧪 How It Works (Summary)

1. Users interact with calculator buttons.

2. The expression is dynamically shown in the top field.

3. On pressing `=`, the custom parser interprets the string and computes the result using `BigDecimal`.

4. The result is displayed in the bottom field.

5. Features like `←` (backspace), `C` (clear), and `+/-` (sign toggle) enhance usability and control.

### ⚠️ Limitations
Despite being robust, the program has a few known limitations:
- ❌ **No Parentheses Support**: Expressions like `(5 + 2) * 3` are not currently supported.
- 🔣 **No Operator Chaining**: Complex expressions requiring multiple operator precedence beyond basic math may not work as expected (e.g., `2^3^2` is not grouped properly).
- ⌛ **No History Log**: Past calculations are not stored or viewable once cleared.
- 🧪 **No Error Handling for Divide by Zero**: While the logic is mostly safe, there's no specific user warning for division by zero errors.
- 🔍 **No Memory Storage**: Lacks features like M+, M-, MR (commonly found in scientific calculators).

### 🛠️ Potential Improvements
If extended further, the following could be added:
- Full expression evaluator with parentheses support
- Memory functionality (M+, MR, MC)
- Theme customization options
- Expression history panel
- Copy/paste support for inputs and results
