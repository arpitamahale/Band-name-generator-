# Band-name-generator-
import tkinter as tk
from tkinter import messagebox

def generate_band_name():
    city = city_entry.get()
    pet = pet_entry.get()
    
    if city and pet:
        band_name = f"{city}_{pet}"
        result_label.config(text=f"Your Band Name: {band_name}", fg="blue")
    else:
        messagebox.showerror("Error", "Please enter both city and pet name!")

# GUI Setup
root = tk.Tk()
root.title("Band Name Generator")
root.geometry("400x300")
root.config(bg="#f0f0f0")

# Heading
tk.Label(root, text="🎵 Band Name Generator 🎵", font=("Arial", 16, "bold"), bg="#f0f0f0").pack(pady=10)

# City Input
tk.Label(root, text="Enter your City:", font=("Arial", 12), bg="#f0f0f0").pack()
city_entry = tk.Entry(root, font=("Arial", 12))
city_entry.pack(pady=5)

# Pet Name Input
tk.Label(root, text="Enter your Pet's Name:", font=("Arial", 12), bg="#f0f0f0").pack()
pet_entry = tk.Entry(root, font=("Arial", 12))
pet_entry.pack(pady=5)

# Generate Button
generate_btn = tk.Button(root, text="Generate Band Name", font=("Arial", 12, "bold"), bg="#008CBA", fg="white", command=generate_band_name)
generate_btn.pack(pady=10)

# Result Label
result_label = tk.Label(root, text="", font=("Arial", 14, "bold"), bg="#f0f0f0")
result_label.pack(pady=10)

# Run App
root.mainloop()
