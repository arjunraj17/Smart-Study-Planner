Problem Statement:

Students and individuals with heavy workloads frequently struggle with prioritization. When faced with multiple assignments, studying for exams, and personal tasks, it is challenging to objectively determine the single most critical task to focus on next.
Traditional to-do lists often rely solely on the deadline, ignoring the crucial factor of estimated effort (the size of the task).
This lack of an objective, effort-and-urgency-aware system leads to procrastination, inefficient time allocation, and increased stress as large, far-off tasks are ignored until they become urgent crises.

Scope of the Project:

In-Scope:
Developing the StudyTask model to hold task details (description, effort, due date).
Implementing the core mathematical prioritization algorithm.
Creating a controller logic (PlannerApp) to manage a list of tasks.
Using Java's native collection sorting capabilities (Lambda expressions and Comparator).
Providing clear, formatted console output (the prioritized list).

Out-of-Scope (Future Enhancements):
User input interface (e.g., accepting new tasks via command line or GUI).
Persistence (saving tasks to a file or database).
Integration with actual date/time APIs.
GUI development (this remains a console application).

Target Users:

The primary target users for this application are individuals managing multiple deadlines and commitments.
University/College Students: Students balancing multiple courses, term papers, exams, and extracurricular activities.
High School Students: Managing varied homework, long-term projects, and test preparation.
Busy Professionals: Individuals who need a quick, objective way to triage daily tasks based on effort and urgency.

High-Level Features:

Feature Name                                         Description

Effort-Urgency Prioritization                        Calculates a single Priority Score based on the ratio of Estimated Effort Hours to Days Until Due.
Immediate Urgency Override                           Ensures tasks due today (Days Until Due \le 0) receive a maximum score to ensure immediate attention.
Task Storage and Retrieval                           Allows programmatic addition of new tasks to an internal list (using ArrayList).
Priority Sorting                                     Sorts the entire task list instantly upon request, ordering from highest to lowest Priority Score.
Formatted Output                                     Presents the resulting prioritized list in a clear, labeled, and easy-to-read table format in the console.
