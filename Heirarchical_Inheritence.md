# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def display_basic(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")


class Employee(Details):
    def __init__(self, name, age, emp_id, department):
        super().__init__(name, age)
        self.emp_id = emp_id
        self.department = department
    def display_employee(self):
        self.display_basic()
        print(f"Employee ID: {self.emp_id}")
        print(f"Department: {self.department}")

class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease
    def display_patient(self):
        self.display_basic()
        print(f"Patient ID: {self.patient_id}")
        print(f"Disease: {self.disease}")


print("Enter Employee details:")
emp_name = input("Name: ")
emp_age = input("Age: ")
emp_id = input("Employee ID: ")
emp_dept = input("Department: ")
employee = Employee(emp_name, emp_age, emp_id, emp_dept)


print("\nEnter Patient details:")
pat_name = input("Name: ")
pat_age = input("Age: ")
pat_id = input("Patient ID: ")
pat_disease = input("Disease: ")
patient = Patient(pat_name, pat_age, pat_id, pat_disease)

print("\nEmployee Information:")
employee.display_employee()

print("\nPatient Information:")
patient.display_patient()

## Sample Output
<img width="667" height="764" alt="image" src="https://github.com/user-attachments/assets/f5ce88aa-20d6-4d32-a560-63f5e742df8d" />

