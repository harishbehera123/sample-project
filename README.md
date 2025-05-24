# sample-project
#its my first repo
import tkinter as tk
from tkinter import messagebox

# Hardcoded user credentials (in a real application, use a secure method!)
USERNAME = "admin"
PASSWORD = "password123"

# Function to check login credentials
def login():
    entered_username = username_entry.get()
    entered_password = password_entry.get()
    
    if entered_username == USERNAME and entered_password == PASSWORD:
        messagebox.showinfo("Login Successful", f"Welcome, {entered_username}!")
    else:
        messagebox.showerror("Login Failed", "Invalid username or password.")

# Create GUI window
root = tk.Tk()
root.title("Login Form")
root.geometry("300x200")

# Username label and entry
tk.Label(root, text="Username").pack(pady=5)
username_entry = tk.Entry(root)
username_entry.pack()

# Password label and entry
tk.Label(root, text="Password").pack(pady=5)
password_entry = tk.Entry(root, show="*")
password_entry.pack()

# Login button
tk.Button(root, text="Login", command=login).pack(pady=20)

# Run the application
root.mainloop()

