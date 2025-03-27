import tkinter as tk

# Function to handle button clicks
def button_click(value):
    current = entry.get()
    entry.delete(0, tk.END)
    entry.insert(tk.END, current + value)

# Function to handle the evaluation of the expression
def evaluate():
    try:
        result = eval(entry.get())
        entry.delete(0, tk.END)
        entry.insert(tk.END, result)
    except Exception as e:
        entry.delete(0, tk.END)
        entry.insert(tk.END, "Error")

# Function to clear the entry field
def clear():
    entry.delete(0, tk.END)

# Creating the main window
root = tk.Tk()
root.title("Calculator")

# Entry widget for displaying input and output
entry = tk.Entry(root, width=16, font=("Arial", 24), borderwidth=2, relief="solid", justify="right")
entry.grid(row=0, column=0, columnspan=4)

# Buttons for digits and operations
buttons = [
    ('7', 1, 0), ('8', 1, 1), ('9', 1, 2), ('/', 1, 3),
    ('4', 2, 0), ('5', 2, 1), ('6', 2, 2), ('*', 2, 3),
    ('1', 3, 0), ('2', 3, 1), ('3', 3, 2), ('-', 3, 3),
    ('0', 4, 0), ('.', 4, 1), ('=', 4, 2), ('+', 4, 3)
]

# Create buttons dynamically
for (text, row, col) in buttons:
    if text == "=":
        button = tk.Button(root, text=text, width=5, height=2, font=("Arial", 20), command=evaluate)
    else:
        button = tk.Button(root, text=text, width=5, height=2, font=("Arial", 20), command=lambda t=text: button_click(t))
    button.grid(row=row, column=col)

# Clear button
clear_button = tk.Button(root, text="C", width=5, height=2, font=("Arial", 20), command=clear)
clear_button.grid(row=5, column=0, columnspan=4)

# Run the application
root.mainloop()
