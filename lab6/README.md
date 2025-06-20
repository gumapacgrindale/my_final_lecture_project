# 🧾 Lab Activity 6: To-Do List Application (Java Swing)

## 📌 Description

This Java program implements a **simple To-Do List** application using the **Swing GUI toolkit**. It consists of two windows:
1. A **task viewer** window that displays a list of tasks in a table.
2. A **task form** window that allows users to input new tasks with a name, description, and status.

This activity demonstrates how to create interactive, form-based desktop applications using Java Swing components.

## 📂 File
- `LabActivity6SwingToDoList.java`

## 🧠 New Concepts Used

This activity introduces the **Java Swing library**, which allows the creation of modern GUI applications with more flexibility and styling than AWT.

### 📂 `JFrame` for Multiple Windows

- Two separate windows (`JFrame`) are used:
  - **Main Viewer Window** (`frameViewer`) – displays tasks and a button to open the form
  - **Form Window** (`frameForm`) – provides inputs for task creation
  
    ```java
    frameViewer = new JFrame("To-Do List Viewer");
    frameForm = new JFrame("Add New Task");
    ```

### 🧾 `JTable` with `DefaultTableModel`
- Displays the list of tasks in a table with three columns:
  - Task Name
  - Task Description
  - Status
  
    ```java
    tableModel = new DefaultTableModel(columnNames, 0);
    table = new JTable(tableModel);
    ```

### ✍️ Swing Form Components
- `JTextField` for Task Name input
- `JTextArea` (with scroll and wrap) for multi-line Task Description
- `JComboBox` for choosing the Task Status from predefined options
- `JButton` to submit the form

  ```java
  JTextField tfTaskName = new JTextField();
  JTextArea taTaskDescription = new JTextArea();
  JComboBox<String> comboBox = new JComboBox<>(statusOptions);
  ```

### 📌 Input Validation and User Feedback
- Ensures task name and description are filled in before allowing submission
- Uses JOptionPane.showMessageDialog() to show an error dialog if fields are incomplete

  ```java
  if (taskName.isEmpty() || taskDescription.isEmpty()) {
      JOptionPane.showMessageDialog(...);
  }
  ```

### ➕ Dynamic Table Update
- Once the form is submitted with valid data, the task is added as a new row in the table using `addRow()`

  ```java
  tableModel.addRow(data);
  ```

### 🔄 Frame Management
- Prevents multiple form windows from being opened simultaneously by checking if the form is already visible:

  ```java
  if (frameForm == null || !frameForm.isVisible()) {
      showTaskForm();
  }
  ```

## 💻 How It Works (Step-by-Step)
1. The program opens the To-Do List Viewer window with a button labeled “Add Task.”

2. When clicked, a form window opens where users can enter:
    - Task Name
    - Task Description
    - Status (Not Started, Ongoing, Completed)

3. When Save Task is clicked:
    - The input is validated
    - The task is added to the table in the viewer window
    - The form window closes

4. Users can repeat the process to add more tasks.

## 🧪 Sample Output
```
+----------------+---------------------------+-------------+
| Task Name      | Task Description          | Status      |
+----------------+---------------------------+-------------+
| Java Project   | Finish calculator module  | Ongoing     |
| Grocery List   | Buy eggs, milk, and rice  | Not Started |
+----------------+---------------------------+-------------+
```

## 🔧 Practical Use
This lab introduces a real-world use case: task management systems. It demonstrates:
- Swing GUI development
- Form validation and user feedback
- Dynamic table interaction
- Multi-window application structure

These concepts are essential for developing productivity tools, inventory systems, project dashboards, and more.
