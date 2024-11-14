# python
tasks = {}  # Dictionary to store tasks; key is task ID, value is task details  

def add_task(task_id, title, description, due_date):  
    tasks[task_id] = {"title": title, "description": description, "due_date": due_date, "status": "open"}  

def update_task_status(task_id, status):  
    if task_id in tasks:  
        tasks[task_id]["status"] = status  
    else:  
        print("Task not found.")  

def view_tasks():  
    for task_id, task_details in tasks.items():  
        print(f"Task ID: {task_id}")  
        print(f"  Title: {task_details['title']}")  
        print(f"  Description: {task_details['description']}")  
        print(f"  Due Date: {task_details['due_date']}")  
        print(f"  Status: {task_details['status']}")  
        print("-" * 20)  
