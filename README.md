# python

tasks = {}  # Dictionary to store tasks; key is task ID, value is task details  

def add_task(task_id, title, description, due_date):  
    tasks[task_id] = {  
        "title": title,  
        "description": description,  
        "due_date": due_date,  
        "status": "open"  
    }  

def update_task_status(task_id, status):  
    if task_id in tasks:  
        tasks[task_id]["status"] = status  
    else:  
        print("Error: Task not found.")  

def view_tasks():  
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

# Example usage:  
add_task(1, "Buy groceries", "Need to buy milk and eggs", "2024-11-20")  
add_task(2, "Complete project", "Finish the final report", "2024-12-01")  
view_tasks()  
update_task_status(1, "completed")  
view_tasks() 
