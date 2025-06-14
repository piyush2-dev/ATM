def atm():
    print("Welcome to XYZ ATM")

    bal = 10000 
    
    while True:
        print("\nA. Deposit")
        print("B. Withdraw")
        print("C. Balance Check")
        print("D. Exit")
        
        choice = input("Enter your choice: ").upper()

        if choice == 'A':
            amount = int(input("Enter amount to deposit: "))
            if amount > 0:
                bal += amount
                print(f"Balance updated. Current Balance: {bal}")
            else:
                print("Invalid deposit amount.")
        
        elif choice == 'B':
            amount = int(input("Enter amount to withdraw: "))
            if amount > bal:
                print("Insufficient Balance.")
            elif amount > 0:
                bal -= amount
                print(f"Cash Withdrawal Successful. Current Balance: {bal}")
            else:
                print("Invalid withdrawal amount.")
        
        elif choice == 'C':
            print(f"Current Balance: {bal}")
        
        elif choice == 'D':
            print("Thank you for using XYZ ATM. Goodbye!")
            break
        
        else:
            print("Invalid choice. Please select A, B, C, or D.")

atm()
