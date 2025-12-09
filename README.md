# Task Tracker CLI

A simple command-line-based to-do list application written in Python.

## Objective

- Add, list, mark complete, and delete tasks.
- Persist tasks using a local `tasks.json` file.
- (Bonus) Support due dates and sort tasks by due date.

## Requirements Implemented

1. **Add a Task**  
   - User can add a task by providing a title and an optional description.
   - Optional due date in `YYYY-MM-DD` format.

2. **List Tasks**  
   - Displays all tasks with their:
     - ID  
     - Title  
     - Description (if any)  
     - Status (`Pending` / `Completed`)  
     - Due date (if any)  
   - Tasks are **sorted by due date**:
     - Tasks with a due date come first (earliest date first).
     - Tasks without a due date appear last.

3. **Mark Task as Completed**  
   - User can update a task’s status to `Completed` using the task ID.

4. **Delete Task**  
   - User can delete a task using its ID.

5. **Data Persistence**  
   - All tasks are stored in and loaded from a local `tasks.json` file.

6. **Bonus Features**  
   - Support for optional due dates.
   - Listing sorts tasks by due date.

## Project Structure

```text
task_tracker/
│
├── main.py           # CLI entry point
├── task_manager.py   # Functions to add, delete, mark complete, sort
├── storage.py        # Functions to read/write JSON file
├── tasks.json        # Stores task data
└── README.md         # Instructions & how to run
