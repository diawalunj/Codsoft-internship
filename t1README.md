## To-Do List Application

This application is a simple To-Do List built using Python and Tkinter. It allows users to add, remove, mark tasks as completed, and list all tasks. The GUI (Graphical User Interface) provides an easy-to-use interface for managing tasks.

### Code Explanation

The application is structured into two main classes: `Task` and `ToDoListApp`.

#### Task Class

The `Task` class represents an individual task with a title, description, and completion status.

- `__init__(self, title, description='')`: Initializes a new task with a title and an optional description. The task is marked as not completed by default.
- `__str__(self)`: Returns a string representation of the task, showing the title, description, and status (Completed or Pending).

#### ToDoListApp Class

The `ToDoListApp` class is the main application class that inherits from `tk.Tk`. It sets up the GUI and manages the list of tasks.

- `__init__(self)`: Initializes the application window, sets the title and size, and configures the background color to a very light blue (`#E0FFFF`). It also creates the listbox for displaying tasks and the buttons for various operations, all colored pink.

- `add_task(self)`: Adds a new task to the list. The task title is taken from the entry field. If the title is empty, a warning message is shown.

- `remove_task(self)`: Removes the selected task from the list. If no task is selected, a warning message is shown.

- `update_task(self)`: Marks the selected task as completed. If no task is selected, a warning message is shown.

- `list_tasks(self)`: Lists all tasks in the listbox. It clears the current list and repopulates it with the updated tasks.

### User Interface Components

- **Task Listbox (`self.task_listbox`)**: Displays the list of tasks.
- **Task Entry (`self.add_task_entry`)**: Allows the user to input a new task title.
- **Add Task Button (`self.add_task_button`)**: Adds the task entered in the task entry to the list. Background color is pink.
- **Remove Task Button (`self.remove_task_button`)**: Removes the selected task from the list. Background color is pink.
- **Mark as Completed Button (`self.update_task_button`)**: Marks the selected task as completed. Background color is pink.
- **List Tasks Button (`self.list_tasks_button`)**: Lists all tasks in the listbox. Background color is pink.

### Running the Application

To run the application, execute the script. The GUI window will open, allowing you to manage your tasks.

```python
if __name__ == "__main__":
    app = ToDoListApp()
    app.mainloop()
