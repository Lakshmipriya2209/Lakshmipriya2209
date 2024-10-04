import tkinter as tk

def add_task():
    task = entry.get()
    if task:
        listbox.insert(tk.END, task)
        entry.delete(0, tk.END)

def delete_task():
    listbox.delete(tk.ANCHOR)

app = tk.Tk()
app.title("Simple To-Do List")

entry = tk.Entry(app, width=30)
entry.pack(pady=10)

add_btn = tk.Button(app, text="Add Task", command=add_task)
add_btn.pack(pady=5)

listbox = tk.Listbox(app, width=30, height=5)
listbox.pack(pady=10)

delete_btn = tk.Button(app, text="Delete Task", command=delete_task)
delete_btn.pack(pady=5)

app.mainloop()
