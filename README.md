print("Welcome to Onkgopotse's Calculator!")
print("Select an operation:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (*)")
print("4. Division (/)")

# Ask user to choose an operation
choice = input("Enter choice (1/2/3/4): ")

# Ask for numbers
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

# Perform calculation based on choice
if choice == '1':
    print(f"The result is: {num1 + num2}")
elif choice == '2':
    print(f"The result is: {num1 - num2}")
elif choice == '3':
    print(f"The result is: {num1 * num2}")
elif choice == '4':
    if num2 != 0:
        print(f"The result is: {num1 / num2}")
    else:
        print("Error! Cannot divide by zero.")
else:
    print("Invalid choice. Please select 1, 2, 3, or 4.")
