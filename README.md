# ATM-Simulation
from atm import display_balance, deposit, withdraw, show_statement

print("\n  ========== Welcome to Python ATM ==========")

while True:
    print("\n  ----------- MAIN MENU -----------")
    print("  1. Display Balance")
    print("  2. Deposit Money")
    print("  3. Withdraw Money")
    print("  4. Transaction Statement")
    print("  5. Exit")
    print("  ---------------------------------")

    choice = input("  Enter your choice (1-5): ").strip()

    if choice == "1":
        display_balance()

    elif choice == "2":
        try:
            amount = float(input("  Enter amount to deposit: Rs. "))
            deposit(amount)
        except ValueError:
            print("\n  Invalid input. Please enter a numeric value.")

    elif choice == "3":
        try:
            amount = float(input("  Enter amount to withdraw: Rs. "))
            withdraw(amount)
        except ValueError:
            print("\n  Invalid input. Please enter a numeric value.")

    elif choice == "4":
        show_statement()

    elif choice == "5":
        print("\n  Thank you for using Python ATM. Goodbye!\n")
        break

    else:
        print("\n  Invalid choice. Please select between 1 and 5.")
