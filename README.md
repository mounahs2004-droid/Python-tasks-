# Python-tasks-
Modular calculator application built using Python to demonstrate functions, default arguments, error handling, and clean code design.

# Modular Calculator in Python(Task 5)

## Description
This project demonstrates functions and modular programming in Python.
It includes basic calculator operations with proper error handling.

## Features
- Add, Subtract, Multiply, Divide
- Modular functions
- Default arguments
- Division by zero handling
- User-friendly menu

## Tools Used
- Python
- VS Code

## How to Run
python calculator.py

# Python Collections Demo(python task 6)

## Description
This project demonstrates the usage of Python collections: List, Tuple, and Set.
It includes common operations such as adding, removing, sorting, removing duplicates,
and performing set operations.

## Concepts Covered
- List operations
- Tuple (immutable data)
- Set operations (union, intersection, difference)
- Mutable vs Immutable collections
- Iteration techniques

## Tools Used
- Python
- VS Code

## How to Run
python collections_demo.py

# TASK 7: Dictionaries & JSON Handling (Python)

## 📌 Objective
The goal of this task is to understand and implement Python dictionaries and JSON handling, including storing structured data, performing CRUD operations, and reading/writing JSON files.

---

## 🛠 Tools Used
- Python
- VS Code
- GitHub

---

## 📂 Files Included
- `student_records.py` – Python script demonstrating dictionary and JSON operations
- `students.json` – JSON file generated from the dictionary
- `README.md` – Task explanation and usage details

---

## 📖 Task Implementation
The following operations are implemented in this project:

1. Created a dictionary to store student details
2. Accessed dictionary keys and values
3. Updated student records
4. Deleted entries from the dictionary
5. Iterated through dictionary data
6. Converted dictionary data into JSON format
7. Saved JSON data to a file
8. Read JSON data back into Python
9. Displayed clean and formatted output

---

## ▶️ How to Run the Project
1. Clone the repository
2. Open the project in VS Code
3. Run the file:
   ```bash
   python student_records.py

import json

# 1. Store student details using dictionary
students = {
    101: {
        "name": "Asha",
        "age": 20,
        "course": "Python",
        "marks": 88
    },
    102: {
        "name": "Ravi",
        "age": 21,
        "course": "Data Science",
        "marks": 92
    }
}

# 2. Access keys and values
print("Student IDs:", students.keys())
print("Student Details:", students.values())

# 3. Update an entry
students[101]["marks"] = 90

# 4. Delete an entry
del students[102]

# 5. Loop through dictionary
print("\nStudent Records:")
for sid, details in students.items():
    print(f"ID: {sid}")
    for key, value in details.items():
        print(f"  {key}: {value}")

# 6. Convert dictionary to JSON and save to file
with open("students.json", "w") as file:
    json.dump(students, file, indent=4)

print("\nData saved to students.json")

# 7. Read JSON back into Python
with open("students.json", "r") as file:
    loaded_data = json.load(file)

# 8. Print clean formatted output
print("\nData loaded from JSON:")
for sid, details in loaded_data.items():
    print(f"ID: {sid}")
    for key, value in details.items():
        print(f"  {key}: {value}")

