# 🧾 Midterm Lab Exam: IT Ticket System (Java CLI)

## 📌 Description

This program is a **console-based IT Ticket Management System** that allows users to create, update, and monitor the progress of up to 5 technical support tickets. It simulates a basic help desk system often used in IT departments, where issues are logged, tracked by urgency, and updated as needed.

This lab exam project demonstrates a combination of all essential Java fundamentals covered in **Lab Activities 1 to 3**, and introduces more advanced concepts such as **arrays**, **loops**, and **user input validation**.

## 📂 File
- `MyMidtermLabExam.java`

## ✨ Features

| Feature | Description |
|--------|-------------|
| 🆕 Add Ticket | Collects issue description and urgency, stores in a ticket list (up to 5 total) |
| 🔄 Update Ticket Status | Updates ticket progress (In Progress / Resolved) |
| 📋 Show All Tickets | Displays all stored tickets along with their urgency and status |
| 📊 Generate Report | Summarizes total tickets and counts of pending vs resolved |
| 🔚 Exit Program | Allows user to safely terminate the application |

---

## 🧠 Java Concepts Used

This project integrates core Java programming fundamentals:

### 📥 Scanner for Input
- Uses `Scanner` to receive real-time inputs from the user through the console.

```java
Scanner input = new Scanner(System.in);
```

### 🔁 Looping with `do-while`
- Keeps the main program running until the user explicitly chooses to exit

```java
do {
// Show menu and handle options
} while (userOption != 5);
```

### 🧩 Conditional Logic
- `switch-case` and `if-else` statements are used for menu navigation and validation.

```java
switch (userOption) {
case 1: addTicket(); break;
// ...
}
```

### 📦 2D Array for Data Storage
- Stores each ticket in a 2D `String[][]` array with columns for **issue** **description**, **urgency**, and **status**.

```java
static String[][] ticketList = new String[5][3];
```

### 🔃 Iterative Display with `for` Loop
- Loops are used to print, search, and count tickets dynamically.

```java
for(int i = 0; i < ticketCount; i++) {
      System.out.println(...);
}
```

### ✅ Input Validation
- Ensures valid menu choices, ticket numbers, and status options are enforced before executing logic.

📈 Simple Report Generation
- Automatically calculates how many tickets are still open or have been resolved.

## 💻 How It Works (Step-by-Step)
1. The program displays a menu:
- Add Ticket
- Update Ticket Status
- Show All Tickets
- Generate Report
- Exit

2. When the user adds a ticket:
- They input a description and urgency level (Low / Medium / High).
- The system saves it with a default status of "Pending".

3. Tickets can later be updated to:
- "In Progress"
- "Resolved"

4. The report option counts:
- How many tickets are pending or in progress
- How many tickets are fully resolved

## 🧪 Sample Output
```
=== IT Ticket System ===
1. Add Ticket
2. Update Ticket Status
3. Show All Tickets
4. Generate Report
5. Exit
Enter choice: 1
Enter issue description: Printer not working
Enter urgency level (Low / Medium / High): High
Ticket successfully added!
```
```
--- All Tickets ---
1. [High] Printer not working - Status: In Progress  
2. [Medium] Internet connection is slow - Status: Pending  
3. [Low] Request for software update - Status: Resolved  
4. [High] System crash during login - Status: In Progress  
5. [Medium] Keyboard not functioning - Status: Pending 
```
```
--- All Tickets ---
1. [High] Printer not working - Status: In Progress  
2. [Medium] Internet connection is slow - Status: Pending  
4. [High] System crash during login - Status: In Progress  
5. [Medium] Keyboard not functioning - Status: Pending  
Enter ticket number to update: 2  
Enter new status (In Progress / Resolved): Resolved  
Ticket status updated.
```
```
--- Ticket Report ---
Total Tickets: 3
Pending Tickets: 2
Resolved Tickets: 1
```

## 🛠️ Practical Use
This program mimics a real-life IT service desk application. It helps beginner developers learn how to:
- Build menu-driven applications
- Use arrays to store multiple data sets
- Apply real-world logic flow
- Incorporate modular programming via methods

Such concepts are foundational for developing:
- Customer service tools
- Bug tracking systems
- Case management dashboards

## ⚠️ Limitations
- 🔢 Fixed array size: Only 5 tickets can be stored.
- 📋 No persistent data storage: Data is lost after program ends (no file or database).
- 🧠 Limited status options: No customizable or detailed workflow stages.
- 🧑‍💻 Single user input only: Lacks user authentication or multi-user functionality.
