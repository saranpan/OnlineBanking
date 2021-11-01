---
#  Online Bank Account Application 
---
> using Object-oriented programming (OOP) in Python 

[![open in colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/wallik2/Tiny_project/blob/main/Bank_Account_OOP_Project_(Level_1).ipynb#scrollTo=ZdUfBFQXa2k-)

It is undeniable to do everything about financial with just your one finger with your online banking, So, our inspiration istry to create the framework of the online banking account.

That's a brief story of how we begin this project, to not waste more of your time, let's skip to our framework

## Bank Account Framework 
---
##### 1. Create a bank account

- Input must be 'name' , 'surname' , 'amount of money' respectively
```sh
# {name:Nuchpol , surname : Rapas , amount : 500}
'Nuchpol_Acc = BankAccount('Nuchpol','Rapas',500)''
```

Now, it will ask you to choose between 'saving account' or 'fixed deposit account'

---
##### 2. Check your bank account status

- Check balance
```sh
# currently Nuchpol has 500$ 
Nuchpol_Acc.balance
> 500
''
```

- Withdraw
```sh
# Now, Nuchpol want to withdraw 100$ 
Nuchpol_Acc.withdraw(100)
> 500
```

If you recheck your balance, Now, Nuchpol remains 500-100 = 400
```sh
# currently Nuchpol has (500 - 100)$ 
Nuchpol_Acc.balance
> 400
```

- Deposit

```sh
# Now, Nuchpol deposit 200$ 
Nuchpol_Acc.deposit(200)
```
If you recheck your balance, Now, Nuchpol remains 400 + 200 = 600
```sh
# currently Nuchpol has (400 + 200)$ 
Nuchpol_Acc.balance
> 600
```

- Check the type of Bank account 

To make sure which type of your banking account now
```sh
# Let say you open the bank account as' Fixed deposit Account' 
Nuchpol_Acc.Check_Status()
> Fixed deposit Account 
```

---
##### 3. Transfer
This can happen there are 2 accounts or more

```sh
Saran_Acc = BankAccount('Saran','Pannasuriyaporn',500)
Kasem_Acc = BankAccount('Kasemwat','Faros',200)

#Here's dictionary stores the recipient name as key and account object as value
All_Acc ={'Kasemwat':Nuchpol_Acc, 'Saran':Saran_Acc }
```

Let's say Saran wants to transfer to Kasemwat 200 baht

```sh
amount = 500
recipient = 'Kasemwat'

Saran_Acc.transfer(All_Acc[recipient],amount)
```

You could expect that Saran's bank account must have (500-200)$,while Kasemwat (200+200)$

```sh
Saran_Acc.Check_Balance()
>300
```
while Kasemwat has (200+200)$

```sh
Kasem_Acc.Check_Balance()
>700
```
Make sure you have sufficient money in your bank account before transfer, otherwise it will return 'Insufficient funds !'
```sh
> Insufficient funds ! 
```

---


Our current features are only these simple framework, and we will continue to improve more like 

1. Update balance for the fixed deposit account as time passes 
2. GUI for login to the account (which register by user & pass)
