# redux_tutorial

> **What** Redux is a predictable state container for JavaScript apps


> **Why** Manage state for your app in one place



```javascript
var Bank = function(balance){
  this.balance = balance
}

Bank.prototype.withdraw = function(amount){
  this.balance = this.balance - amount
  return this.balance
}

var bank = new Bank(100)
var withdraw_1 = bank.withdraw(50)
var withdraw_2 = bank.withdraw(50)
console.log(withdraw_1); // 50
console.log(withdraw_2); //  0
```


```javascript
var FBank = function(balance){
  this.balance = balance
}
FBank.prototype.withdraw = function(amount){
  return new FBank ( this.balance - amount)
}

var fBank = new FBank(100)

var fBank_Withdraw_1 = fBank.withdraw(50)
var fBank_Withdraw_2 = fBank.withdraw(50)

console.log(fBank_Withdraw_1.balance)
console.log(fBank_Withdraw_2.balance)

var fBank_Withdraw_3 = fBank_Withdraw_1.withdraw(50)
console.log(fBank_Withdraw_3.balance)
```


# What can you expect here?

- How redux work?

- How you can use redux in real world example

- How you can use redux in real world example?

# Source 

-[Free Videos]()