# VSP
ATM pin validation using while loop
print("Welcome to Lotus Investments Bank Ltd !!!")
print("Please Insert Your ATM card")
print("processing....")
atmpin=2012
chance=3
balance=50000
options=4
inputpin=int(input("Please Enter your four digit pin:"))
while chance>0:
    if inputpin!=atmpin:
      print("Incorrect pin")    
      inputpin=int(input("please re-Enter your four digit pin:"))
      chance=chance-1
    elif inputpin==atmpin:
        print("Login success")
        break
else:
    print("You have done Maximum attempt, Your card is blocked. Please contact your Bank")  
if inputpin==atmpin:
    print("1.Balance")
    print("2.Withdraw")
    print("3.Deposit")
    print("4.cancel")
    options=int(input("Please select Your option, (1, 2, 3, 4): "))
    while options>0:
        if options==1:
            print("Your Current Balance is Rs:", balance)
            options=int(input("Please select Your option, (1, 2, 3, 4): "))
        elif options==2:
            deposit=int(input("Please Enter the amount to deposit Rs: " ))
            balance+=deposit
            print("Deposited amount is Rs:", deposit)
            print("Your Current Balance is Rs:", balance)
            options=int(input("Please select Your option, (1, 2, 3, 4): "))
        elif options==3:
            withdraw=int(input("Please Enter the amount to withdraw Rs: " ))
            balance-=withdraw
            print("withdrawal amount is Rs:", withdraw)
            print("Your Current Balance is Rs:", balance) 
            options=int(input("Please select Your option, (1, 2, 3, 4): "))
        elif options==4:
            print("Exit")
            break
        else:
            print("invalid Entry")
            break       
            options=options
