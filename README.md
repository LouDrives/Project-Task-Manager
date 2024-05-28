							Task Manager

Made by Louay Azouaghe 
Code: 122940

-Introduction

A task management application coded in C. Users can create, update, delete, view, list, and search tasks. Tasks are stored in a text file with fields.

-Design Choices

Data Storage

- File-Based Storage: Tasks saved in `tasks.txt` as plain text. Each task on a line with fields separated by `|`.
- Task Structure: Each task represented by a `Task` struct with ID, title, description, location, due date, and completion status.

Code Organization

- Functions: Organized into functions for specific operations like loading, saving, creating, updating, deleting, showing, listing, and searching tasks.
- Command-Line Interface (CLI): Uses CLI commands for user interaction.

Error Handling

- File Operations: Checks for errors when handling files. Displays appropriate error messages.
- Input Validation: Validates input arguments and provides usage instructions.

How to Run the Program

Prerequisites

- C compiler (e.g., `gcc`)

Compilation

To compile, use:
gcc -o todo main.c


Usage

Run with:
./todo <command> [options]


Commands

- Create a task:
  ./todo create <title> --due_date <YYYY-MM-DD> [--description <desc>] [--location <loc>]
  

- Update a task:
  ./todo update <id> [--title <title>] [--description <desc>] [--location <loc>] [--due_date <YYYY-MM-DD>] [--completed <0|1>]

- Delete a task:
  ./todo delete <id>

- Show a task:
  ./todo show <id>

- List tasks:
  ./todo list [--date <YYYY-MM-DD>]

- Search tasks by title:
  ./todo search <title>

- Help:
  ./todo

If no command provided, the program lists tasks for the current date.

Conclusion

This task management application is a simple tool for managing tasks efficiently. It showcases basic file handling, string manipulation, and command-line argument parsing in C.
