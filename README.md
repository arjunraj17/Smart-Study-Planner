# Smart-Study-Planner
Smart Study Planner: Prioritization App

Project Title

Smart Study Planner

Overview of the Project

The Smart Study Planner is a command-line Java application designed to help students and professionals prioritize their workload effectively. It uses a mathematical model to calculate a Priority Score for each task by factoring in both the estimated effort required and the proximity of the deadline.

This approach ensures that tasks that are both time-consuming and immediately due are flagged as the highest priority, helping the user focus on the most critical item first.

Features

Task Management: Allows adding tasks with three key parameters: description, estimated effort (in hours), and days until due.

Dynamic Prioritization: Automatically calculates a Priority Score for every task using the following core formula:


$$\text{Priority Score} = \left( \frac{\text{Effort Hours}}{\text{Days Until Due}} \right) \times 10$$

Urgency Override: Tasks due today (daysUntilDue <= 0) are assigned a very high priority score (Effort $\times 100$) to guarantee they jump to the top of the list.

Real-time Sorting: Uses Java's Comparator and Lambda expressions for fast, efficient sorting of the task list by the calculated score in descending order.

Prioritized Display: Prints a formatted, easy-to-read table to the console, clearly highlighting the single highest-priority task with a ⭐ NEXT UP tag.

Technologies/Tools Used

Language: Java (Requires JDK 8 or higher)

Core Concepts: Object-Oriented Programming (OOP), Data Structures (ArrayList), and modern Java Collections API features (Lambda Expressions and Comparator).

Steps to Install & Run the Project

Since this is a single-file application, installation is straightforward using a Java Development Kit (JDK).

1. Save the Code

Create a file named PlannerApp.java.

Copy and paste the provided Java code into this file.

2. Compile the Java File

Open your command-line interface (CLI) or terminal and navigate to the directory where you saved the file.

# Compile the Java source file
javac PlannerApp.java


3. Run the Application

Execute the compiled class file using the Java Virtual Machine (JVM).

# Run the compiled application
java PlannerApp


Instructions for Testing

The main method in PlannerApp.java includes a predefined set of sample tasks designed to demonstrate the prioritization logic.

Expected Test Scenario

Run the application and observe the two output tables.

Test Case 1: Initial Tasks
Verify that "Review Java Code" (Score 25.00) is ranked higher than "Final Project - Implementation" (Score 21.43), despite the latter having higher total effort, due to its closer deadline.

Test Case 2: Immediate Urgency
Observe the second output table (after the "SIMULATION" message). The task "Submit Lab Report" (due in 0 days) must immediately jump to the top and be marked with ⭐ NEXT UP, demonstrating the urgency override logic.

Screenshots (Console Output Simulation)

Initial Prioritized List

==========================================================================
SMART STUDY PLANNER: RECOMMENDED PRIORITY LIST
==========================================================================
Task Description                         | Effort: 2 hrs | Due In: 2 days | Priority Score: 25.00
--------------------------------------------------------------------------
   NEXT UP: Review Java Code             | Effort:  5 hrs | Due In:  2 days | Priority Score: 25.00
   Final Project - Implementation        | Effort: 15 hrs | Due In:  7 days | Priority Score: 21.43
   Read Chapter 5 for History            | Effort:  2 hrs | Due In:  1 days | Priority Score: 20.00
   Plan next week's schedule             | Effort:  1 hrs | Due In: 14 days | Priority Score: 0.71
--------------------------------------------------------------------------


Output After Adding Task Due TODAY

--- SIMULATION: Adding a task due TODAY ---
==========================================================================
SMART STUDY PLANNER: RECOMMENDED PRIORITY LIST
==========================================================================
Task Description                         | Effort: 3 hrs | Due In: 0 days | Priority Score: 300.00
--------------------------------------------------------------------------
   NEXT UP: Submit Lab Report            | Effort:  3 hrs | Due In:  0 days | Priority Score: 300.00
   Review Java Code                      | Effort:  5 hrs | Due In:  2 days | Priority Score: 25.00
   Final Project - Implementation        | Effort: 15 hrs | Due In:  7 days | Priority Score: 21.43
   Read Chapter 5 for History            | Effort:  2 hrs | Due In:  1 days | Priority Score: 20.00
   Plan next week's schedule             | Effort:  1 hrs | Due In: 14 days | Priority Score: 0.71
--------------------------------------------------------------------------
