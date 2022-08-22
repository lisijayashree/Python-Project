# Python-Project
OOPS
class Atm:
    def __init__(self):
        self.__pin=""
        self.__balance=0
        self.operation()
        #print(id(self))
        #self.operation()
    def operation(self):
        user_input=input("""How would you like to proceed
        1.Enter 1 to create pin
        2.Enter 2 to deposit
        3.Enter 3 to withdraw
        4.Enter 4 to Check_balance
        5.Enter 5 to exit""")
        
        if user_input=="1":
            print("Enter pin")
            self.create_pin()
        elif user_input=="2":
            print("Deposit")
            self.deposit()
        elif user_input=="3":
            print("Withdraw")
            self.withdraw()
        elif user_input=="4":
            print("Check_balance")
            self.check_balance()
        else:
            print("Thank you")
    def create_pin(self):
        self.__pin=int(input())
        print("Pin Created Sucessfully")
        self.operation()
    def deposit(self):
        temp=int(input("enter pin"))
        if temp==self.__pin:
            amt=int(input("Enter Amout"))
            self.__balance=amt+self.__balance
            print("Deposit sucefully")
        else:
            print("Invalid pin")
        self.operation()
    def withdraw(self):
        temp=int(input("Enter pin"))
        if temp==self.__pin:
            amt=int(input("enter amount"))
            if amt<self.__balance:
                self.__balance=self.__balance-amt
                print("Operation sucessfully")
            else:
                print("Not enough balance")
        else:
            print("Invalid pin")
        self.operation()
    def check_balance(self):
        temp=int(input("enter pin"))
        if temp==self.__pin:
            print(self.__balance)
        else:
            print("Invalid Pin")
            
>>>
sbi=Atm()
