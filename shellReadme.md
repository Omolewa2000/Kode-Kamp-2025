# Shell Fundamentals - Interactive To-Do List Manager

This is a simple, interactive command-line To-Do List manager built with Bash scripting. This project demonstrates fundamental shell scripting concepts including user input handling, file operations, loops, and conditional statements.

## Features

- 📝 **Add Tasks**: Create new tasks and save them to your personal to-do list
- 👀 **View Tasks**: Display all your tasks with numbered lines for easy reference
- ❌ **Delete Tasks**: Remove specific tasks by their number
- 💾 **Persistent Storage**: Tasks are saved in `~/todo.txt` and persist between sessions
- 🔄 **Interactive Loop**: Continuous operation until you choose to exit
- ✅ **Input Validation**: Handles invalid inputs gracefully


![create the script](screenshot/image-10.png)

I created the script using the vi editor

I also made the script executable by running the command chmod +x todo.sh


### 2. Make the Script Executable

```bash
chmod +x todo.sh
```

### 3. Run the To-Do List Manager

```bash
./todo.sh
```

## Usage

When you run the script, you'll see an interactive menu with the following options:

### Initial Menu Display

*The main menu interface showing all available options*

```
=========================================
          TO-DO LIST MANAGER
=========================================
1. View all tasks
2. Add a new task
3. Delete a task1
4. Exit the program
=========================================
```

### Option 1: View All Tasks
- Displays all your current tasks with line numbers
- Shows "No tasks found" if your list is empty

![View Task](screenshot/image-14.png)
*Display of all current tasks with numbered lines*

### Option 2: Add a New Task
- Prompts you to enter a new task
- Saves the task to `~/todo.txt`
- Validates that the task is not empty

![Add Task](screenshot/image-15.png)
*Demonstration of adding a new task to the to-do list*

### Option 3: Delete a Task
- Shows your current tasks with numbers
- Prompts you to enter the number of the task to delete
- Validates the input and confirms deletion

![Delete Task](screenshot/image-16.png)
*Process of deleting a specific task by its number*


### Option 4: Exit
- Safely exits the program
- Shows where your tasks are saved

![Exit Program](screenshot/image-17.png)
*Exit message showing where tasks are saved*

## Technical Implementation

### Key Bash Features Used

- **Variables**: `TODO_FILE="$HOME/todo.txt"`
- **User Input**: `read` command for interactive input
- **File Operations**: `echo >>`, `touch`, file existence checks
- **Text Processing**: `nl` for line numbers, `sed` for deletion
- **Loops**: `while true` for continuous operation
- **Conditionals**: `case` statements and `if` conditions
- **Input Validation**: Number validation and range checking

### File Structure

```
shell-fundamentals/
├── todo.sh          # Main script file
├── ShellReadme.md        # This documentation
└── ~/todo.txt       # Generated task storage file (in user's home directory)
```

## 🛠️ How to Run

```bash

./todo.sh
```

## Requirements

- **Bash**: Version 4.0 or higher
- **Linux/macOS**: Compatible with most Unix-like systems
- **Permissions**: Write access to home directory

## License

This project is open source and available under the [MIT License](LICENSE).



---
"The key is not to prioritize what's on your schedule, but to schedule your priorities."
— Stephen R. Covey

*Happy task managing! 📝*
