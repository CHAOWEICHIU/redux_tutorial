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

# What can you expect here?

- How redux work?

- How you can use redux in real world example

- How you can use redux in real world example?

# Source 

-[Free Videos]()