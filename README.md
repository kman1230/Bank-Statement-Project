# Bank-Statement-Project
class ChaseBank Customer:
  def __init__(self, name, balance):
    self.name = name
    self.balance = balance
    
    """Withdraw money from  customer's bank account"""
   def withdraw(self, amount):
       if amount > self.balance:
           print(RuntimeError('Amount greater than balance'))
       self.balance -= amount
       return self.balance

    """Deposits money to customer's bank account"""

   def deposit(self, amount):
       self.balance += amount
       return self.balance

   def __str__(self):
       return "{} : {}".format(self.name, self.balance)


customer_1 = ChaseBank_Customer("Jim", 5000)
customer_2 = ChaseBank_Customer("Chris", 200)
customer_3 = ChaseBank_Customer("Moe", 1000)

customer_3.withdraw(500)
print(customer_3)
customer_3.withdraw(600)
print(customer_3)
print(customer_1)
