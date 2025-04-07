# BasicPy-Calculator
# Simple Python calculator program to prompt user input and operation


print("Basic Calculator program!")

# Get user input for two numbers
try:
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))
except ValueError:
    print("Invalid input! Please enter numeric values.")
    exit()

# Get user input for the operation
operation = input("Enter the operation (+, -, *, /): ")

# Perform the calculation based on the operation
result = None
if operation == '+':
    result = num1 + num2
elif operation == '-':
    result = num1 - num2
elif operation == '*':
    result = num1 * num2
elif operation == '/':
    if num2 == 0:
        print("Error: Division by zero is not allowed!")
        exit()
    else:
        result = num1 / num2
else:
    print("Invalid operation! Please use one of: +, -, *, /")
    exit()

# Display the result
print(f"Result: {num1} {operation} {num2} = {result}")
