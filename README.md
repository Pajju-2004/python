# Dictionary to store tasks; key is task ID, value is task details
tasks = {}

def add_task(task_id, title, description, due_date):
    """Add a new task to the task dictionary."""
    tasks[task_id] = {
        "title": title,
        "description": description,
        "due_date": due_date,
        "status": "open"
    }
    print(f"Task '{title}' added successfully!")

def update_task_status(task_id, status):
    """Update the status of an existing task."""
    if task_id in tasks:
        tasks[task_id]["status"] = status
        print(f"Task ID {task_id} status updated to '{status}'.")
    else:
        print("Error: Task not found.")

def view_tasks():
    """Display all tasks in the task dictionary."""
    if not tasks:
        print("No tasks found.")
    else:
        for task_id, task_details in tasks.items():
            print(f"Task ID: {task_id}")
            print(f" Title: {task_details['title']}")
            print(f" Description: {task_details['description']}")
            print(f" Due Date: {task_details['due_date']}")
            print(f" Status: {task_details['status']}")
            print("-" * 20)

# Example usage
add_task(1, "Complete assignment", "Finish the math assignment", "2024-11-20")
add_task(2, "Buy groceries", "Buy milk, eggs, and bread", "2024-11-15")
view_tasks()
update_task_status(1, "completed")
view_tasks()



