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

## How to Run

Prerequisites:

- Python 3.7 or newer installed.
- (Optional) Create and activate a virtual environment:

  python -m venv .venv
  source .venv/bin/activate  # macOS / Linux
  .\.venv\Scripts\activate   # Windows (PowerShell)

Run the CLI:

- From the repository root, run the main script with Python:

  python main.py

Common usage examples (these are typical commands; adapt flags if your implementation differs):

- Add a task:

  python main.py add "Buy groceries" --description "Milk, eggs, bread" --due 2025-12-31

- List tasks:

  python main.py list

- Mark a task as completed (replace <id> with the task ID shown in list):

  python main.py complete <id>

- Delete a task (replace <id> with the task ID):

  python main.py delete <id>

Notes:

- Tasks are stored in `tasks.json` in the project root. If the file doesn't exist it will be created automatically on first write.
- If your CLI uses different subcommands or flags, adapt the example commands above to match your implementation.

## Project Structure

```text
task_tracker/
│
├── main.py           # CLI entry point
├── task_manager.py   # Functions to add, delete, mark complete, sort
├── storage.py        # Functions to read/write JSON file
├── tasks.json        # Stores task data
└── README.md         # Instructions & how to run

```
