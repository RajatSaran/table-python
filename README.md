
while active:
    try:
        num = int(input("Enter a number (1-10): "))
        if is_valid_input(num):
            table = [num * i for i in range(1, 11)]
            print("Multiplication Table:")
            for i in range(1, 11):
                print(f"{num} x {i} = {table[i-1]}")
            
            rerun = input("Do you want to calculate another table? (yes/no): ")
            if rerun.lower() != 'yes':
                active = False 
        else:
            print("Invalid input. Please enter a number between 1 and 10.")
    except ValueError:
        print("Invalid input. Please enter a valid number.")

print("Thank you for using the program!")
