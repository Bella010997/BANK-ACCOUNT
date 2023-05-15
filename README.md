# BANK-ACCOUNT
import sys

from users import User
from accounts import Account

class Bank:
    def __init__(self):
        self.accno = ""
        self.name = ""
        self.acc_type = ""
        self.balance = 0
        self.sc = sys.stdin

    def create_account(self, name, pass_code):
        self.name = name
        self.pass_code = pass_code
        self.ac_no += 1
        return True
   
    def openAccount(self):
        print("Enter Account No: ", end="")
        self.accno = input()
        print("Enter Account type: ", end="")
        self.acc_type = input()
        print("Enter Name: ", end="")
        self.name = input()
        print("Enter Balance: ", end="")
        self.balance = int(input())
    
    def showAccount(self):
        print("Name of account holder: " + self.name)
        print("Account no.: " + self.accno)
        print("Account type: " + self.acc_type)
        print("Balance: " + str(self.balance))
    
    def deposit(self):
        amt = 0
        print("Enter the amount you want to deposit: ")
        amt = int(input())
        self.balance = self.balance + amt
    
    def withdrawal(self):
        amt = 0
        print("Enter the amount you want to withdraw: ")
        amt = int(input())
        if (self.balance >= amt):
            self.balance = self.balance - amt
            print("Balance after withdrawal: " + str(self.balance))
        else:
            print("Insufficient balance")
    def balance(self):
        self.balance = self.balance + amt
        total += amount
        balance -= amount
        print(f'Your balance is {balance}')
    def deleteAccount(self):
       name = input("\n Please input customer name you want to delete :\n")
       user_account = self.search_customers_by_name(name)
    if user_account !=None: 
          print ("The customer does not exist")
      else: 
          self.customers_list.remove(name)    
    def login_account(self, name, pass_code):
        if self.name == name and self.pass_code == pass_code:
            return True
        else:
            return False

if __name__ == "__main__":
    bankManagement = Bank()
    while True:
        print("\n ->||    Welcome to InBank    ||<- \n")
        print("1)Create Account")
        print("2)Login Account")
        print("3)Deposit")
        print("4)Withdrawal")
        print("5)Balance")
        print("6)Delete account")
        
        try:
            ch = int(input("\n    Enter Input:"))
            if ch == 1:
                try:
                    name = input("Enter Unique UserName:")
                    pass_code = int(input("Enter New Password:"))
                    if bankManagement.create_account(name, pass_code):
                        print("MSG : Account Created Successfully!\n")
                except:
                    print("Invalid Input")
            elif ch == 2:
                try:
                    name = input("Enter UserName:")
                    pass_code = int(input("Enter Password:"))
              
                  elif ch == 3:
                try:
                    name = input("Enter UserName:")
                    pass_code = int(input("Enter Password:"))
                  deposit(self)
                  elif ch == 4:
                try:
                    name = input("Enter UserName:")
                    pass_code = int(input("Enter Password:"))
                  withdrawal(self)
                  elif ch == 5:
                try:
                    name = input("Enter UserName:")
                    pass_code = int(input("Enter Password:"))
                  balance(self)
                  elif ch == 6:
                try:
                    name = input("Enter UserName:")
                    pass_code = int(input("Enter Password:"))
                  deleteAccount(self)
                    if bankManagement.login_account(name, pass_code):
                        print("MSG : Login Successful!\n")
                    else:
                        print("MSG : Invalid Credentials!\n")
                except:
                    print("Invalid Input")
            else:
                print("Invalid Input")
        except:
            print("Invalid Input")
class Bank:
    def __init__(self):
        self.total = 100
        
    def withdrawn(self, name, withdrawal):
        if self.total >= withdrawal:
            print(name + " withdrawn " + str(withdrawal))
            self.total -= withdrawal
            print("Balance after withdrawal: " + str(self.total))
            
            import time
            time.sleep(1)
            
        else:
            print(name + " you can not withdraw " + str(withdrawal))
