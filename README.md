# KAKU-YAYNI-CLYDE-MANLAPAZ-

account1 = ["1001", "Juan", 1111, 5000]
account2 = ["1002", "Maria", 2222, 10000]

print(" === SIMPLE ATM ===")

account_number = input("Enter Account Number: ")
pin = int(input("Enter PIN: "))

if account_number == account1[0] and pin == account1[2]:
    print(f"Welcome {account1[1]}")
    print(f"Balance: {account1[3]}")

    print("1. Deposit")
    print("2. Withdraw")

    choice = int(input("Enter Your Choice: "))
    if choice == 1:
        print("Deposit")
        amount = float(input("Enter Deposit Amount: "))

        if amount > 0:
            account1[3] = account1[3] + amount
            print("Deposit Successful ")
            print(f"New Balance: {account1[3]:.2f}")
        else:
            print("Invalid Amount")


    elif choice == 2:
        print("Withdraw")
        amount = float(input("Enter Withdrawal Amount: "))

        if amount > 0 and amount <= account1[3]:
            account1[3] = account1[3] - amount
            print("Withrawal Successfull! ")
            print(f"New Balance: {account2[3]:.2f}")
        elif amount <= 0 or amount > account1[3]:
            print("Insufficient Balance!")
        else:
            print("Invalid Choice!")


    else:
        print("Invalid Choice")



elif account_number == account2[0] and pin == account2 [2]:
    print(f"Welcome {account2[1]}")
    print(f"Balance: {account2[3]}")

    print("1. Deposit")
    print("2. Withdraw")

    choice1 = int(input("Enter Your Choice: "))
    if choice1 == 1:
        print("Deposit")
        amount = float(input("Enter Deposit Amount: "))

        if amount > 0:
            account2[3] = account2[3] + amount
            print("Deposit Successful ")
            print(f"New Balance: {account2[3]:.2f}")
        else:
            print("Invalid Amount")


    elif choice1 == 2:
        print("Withdraw")
        amount = float(input("Enter Withdrawal Amount: "))

        if amount > 0 and amount <= account1[3]:
            account1[3] = account1[3] - amount
            print("Withrawal Successfull! ")
            print(f"New Balance: {account2[3]:.2f}")
        elif amount <= 0 or amount > account1[3]:
            print("Insufficient Balance!")
        else:
            print("Invalid Choice!")



    else:
        print("Invalid Choice")


else:
    print("Invalid Account Number or PIN")
