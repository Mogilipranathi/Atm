import time

print("Please insert your CARD")
time.sleep(5)

password = 1234
balance = 5000

# Ask for the PIN
pin = int(input("Enter your ATM PIN: "))

# Verify PIN
if pin == password:
    while True:
        # Display options
        print("""
        1 == Check Balance
        2 == Withdraw Balance
        3 == Deposit Balance
        4 == Exit
        """)

        try:
            option = int(input("Please enter your choice: "))
        except ValueError:
            print("Please enter a valid option.")
            continue

        # Handle options
        if option == 1:
            print(f"Your current balance is: {balance}")

        elif option == 2:
            withdraw_amount = int(input("Please enter withdrawal amount: "))
            if withdraw_amount <= balance:
                balance -= withdraw_amount
                print(f"{withdraw_amount} is debited from your account.")
                print(f"Your current balance is: {balance}")
            else:
                print("Insufficient balance.")

        elif option == 3:
            deposit_amount = int(input("Please enter deposit amount: "))
            balance += deposit_amount
            print(f"{deposit_amount} is credited to your account.")
            print(f"Your updated balance is: {balance}")

        elif option == 4:
            print("Thank you for using the ATM. Goodbye!")
            break

        else:
            print("Invalid option. Please try again.")
else:
    print("Incorrect PIN. Please try again.")
