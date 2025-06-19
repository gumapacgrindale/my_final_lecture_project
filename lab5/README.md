# 🧾 Lab Activity 5: Quiz Application using Java AWT

## 📌 Description

This Java program is a **GUI-based multiple-choice quiz application** built using the Abstract Window Toolkit (AWT). It allows users to answer a series of predefined questions one at a time. The program validates answers, calculates the score, and displays the final result at the end.

## 📂 File
- `LabActivity5QuizAppAWT.java`

## 🧠 New Concepts Used

This activity introduces advanced GUI techniques using **AWT** and adds logic for interactive quiz applications, including:

### ❓ Dynamic Question and Answer Logic

- Uses `String[]` and `String[][]` arrays to store:
  - `questions`: list of quiz questions
  - `choices`: multiple choice options per question
  - `correctAnswers`: expected correct answers for validation
- A single set of components (`Label`, `Checkbox`, etc.) is **reused and updated** for each question.

### 🎯 Checkbox Grouping with `CheckboxGroup`

- Groups all multiple-choice options so only one can be selected at a time.
  ```java
  optionsGroup = new CheckboxGroup();
  options[i] = new Checkbox("", optionsGroup, false);

### 🔄 Interactive Navigation & Event-Driven Logic
- A **Next** button triggers:
  - Validation of selected answer
  - Score incrementing
  - Moving to the next question or showing final results
- All logic is placed inside an `ActionListener`:
  ```java
  btnNext.addActionListener(new ActionListener() {
    public void actionPerformed(ActionEvent e) {
        // validate answer and move forward
      }
  });
  
### 🧮 Score Calculation
- A global `score` variable is incremented only when the user selects the correct answer.
  ```java
  if (selected.getLabel().equals(correctAnswers[currentQuestion])) {
    score++;
  }

### 🧾 Result Display and Component Disabling
- When all questions are answered:
  - Displays the final score using `lblQuestion`
  - Disables all checkboxes and the `Next` button to prevent further interaction
  ```java
  showResult();

### 🎨 GUI Styling and Customization
- Components are styled using:
  - Fonts (`Font.BOLD`, `Font.PLAIN`)
  - Colors (`Color.BLUE`)
- Custom methods like `customizedTextBold()` and `customizeCheckbox()` promote code reusability.

## 💻 How It Works (Step-by-Step)

1. When the app starts, it displays the first question and its four choices.

2. The user selects an answer and clicks Next.

3. If no choice is selected, an error message appears.

4. If a choice is selected:
   - The app checks the answer
   - Updates the score
   - Loads the next question

5. After the last question, it displays the final score and disables all interaction.

## 🧪 Sample Output (GUI)
```
Question:
What is also known as the "brain" of the computer?

Options:
[ ] A. Monitor
[ ] B. RAM
[✔] C. CPU
[ ] D. Hardware

→ (after clicking Next…)

Quiz Completed! Your Score: 3 out of 3
```

## 🔧 Practical Use
This application demonstrates how to:
- Create interactive quiz/test interfaces
- Manage application state (e.g., current question, score)
- Validate user input in a graphical setting
- Dynamically update GUI components based on logic

Such skills are foundational for building educational tools, training software, and **assessment apps**.
