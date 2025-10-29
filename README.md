.pydef calculator():
    print("🧮 Welcome to Onkgopotse's Calculator!")
    print("-" * 40)
    print("Select an operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Exit")

    while True:
        choice = input("\nEnter choice (1/2/3/4/5): ")

        if choice == '5':
            print("Goodbye! 👋")
            break

        if choice not in ('1', '2', '3', '4'):
            print("Invalid choice. Please select a valid option (1–5).")
            continue

        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("⚠️ Please enter valid numeric values.")
            continue

        if choice == '1':
            result = num1 + num2
            operation = "+"
        elif choice == '2':
            result = num1 - num2
            operation = "-"
        elif choice == '3':
            result = num1 * num2
            operation = "*"
        elif choice == '4':
            if num2 == 0:
                print("❌ Error: Cannot divide by zero.")
                continue
            result = num1 / num2
            operation = "/"

        print(f"\n✅ {num1} {operation} {num2} = {result}")
        print("-" * 40)

# Run the calculator
calculator()
