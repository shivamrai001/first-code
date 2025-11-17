# CALCULATOR
# Simple Calculator in Python
# Made for 1st Year B.Tech Students ❤️
# Author: Your Name (add your name here)

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero is not allowed."
    else:
        return x / y

# Main calculator program
print("=== Welcome to My First Python Calculator ===")
print("Select operation:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (×)")
print("4. Division (÷)")

while True:
    choice = input("\nEnter choice (1/2/3/4): ")

    if choice in ['1', '2', '3', '4']:
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input! Please enter numbers only.")
            continue

        if choice == '1':
            print(f"{num1} + {num2} = {add(num1, num2)}")

        elif choice == '2':
            print(f"{num1} - {num2} = {subtract(num1, num2)}")

        elif choice == '3':
            print(f"{num1} × {num2} = {multiply(num1, num2)}")

        elif choice == '4':
            result = divide(num1, num2)
            print(f"{num1} ÷ {num2} = {result}")

        # Ask if user wants to do another calculation
        next_calculation = input("\nDo another calculation? (yes/no): ")
        if next_calculation.lower() == "no":
            print("Thank you for using the calculator! See you again! 😊")
            break
    else:
        print("Invalid choice! Please select 1, 2, 3, or 4.")
