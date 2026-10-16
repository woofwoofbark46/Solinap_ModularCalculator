# Solinap_ModularCalculator

This modular calculator lets you divide, subtract, add, and multiply 2 numerical inputs.

It features pressing 1(Addition), 2(Subtraction), 3(Multiplication), 4(Division), and 5 to Exit. 

Finished code below(There are no changes, so this is now the Version 2 of my code)!

# VERSION 2, Modular Calculator
#Input num1, num2

num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))

#Seperate reusable functions
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Cannot divide by zero"
    return x / y

def calculator():
    print("--- Python Calculator ---")

      while True:
        print("\nSelect an operation:")
        print("1. Add (+)")
        print("2. Subtract (-)")
        print("3. Multiply (*)")
        print("4. Divide (/)")
        print("5. Exit")
        
        # Take user selection
        choice = input("Enter choice (1-5): ")
        
        if choice == '5':
            print("Exiting calculator. Goodbye!")
            break
            
        if choice in ('1', '2', '3', '4'):
            try:
                # Take numerical inputs and convert them to floats
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
            except ValueError:
                print("Invalid input. Please enter numbers only.")
                continue
            
            # Perform calculation based on the user's choice
            if choice == '1':
                print(f"Result: {num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"Result: {num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"Result: {num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                print(f"Result: {num1} / {num2} = {divide(num1, num2)}")
        else:
            print("Invalid choice! Please select a valid operation (1-5).")

#Run the calculator
if __name__ == "__main__":
    calculator()
    
