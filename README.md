### Python Weight Converter with GUI using Tkinter

This Python project creates a weight converter GUI that allows users to convert kilograms into grams, ounces, or pounds using Tkinter.

### Prerequisites:
- Install Tkinter (if not already available):
  ```bash
  pip install tk
  ```

### Steps:

1. **Import Required Modules:**
   ```python
   import tkinter as tk
   from tkinter import *
   ```

2. **Create GUI Window:**
   ```python
   window = Tk()
   window.title("Weight Converter")
   window.geometry("400x400")
   ```

3. **Add Input and Buttons:**
   ```python
   Label(window, text="Enter weight in Kgs").pack()
   kg = DoubleVar()
   Entry(window, textvariable=kg).pack()
   Button(window, text="Convert to Gram", command=convert_to_gram).pack()
   Button(window, text="Convert to Ounce", command=convert_to_ounce).pack()
   Button(window, text="Convert to Pound", command=convert_to_pound).pack()
   ```

4. **Conversion Functions:**
   ```python
   def convert_to_gram():
       gram = kg.get() * 1000
       Label(window, text=f"{gram} grams").pack()

   def convert_to_ounce():
       ounce = kg.get() * 35.274
       Label(window, text=f"{ounce} ounces").pack()

   def convert_to_pound():
       pound = kg.get() * 2.20462
       Label(window, text=f"{pound} pounds").pack()
   ```

5. **Run the App:**
   ```python
   window.mainloop()
   ```

### Output:
The program allows users to input a weight in kilograms and displays the converted weight in grams, ounces, or pounds when the corresponding button is clicked.
