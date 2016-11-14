# redux_tutorial

> **What** Redux is a predictable state container for JavaScript apps


> **Why** Manage state for your app in one place






> Imperitive Style

```javascript
var bank 	   = new Bank(100)
  , withdraw_1 = bank.withdraw(50)
  , withdraw_2 = bank.withdraw(50)
console.log(withdraw_1) // 50
console.log(withdraw_2) //  0
```

> Redux Style
```javascript
var redux_bank 			  = new Redux_Bank(100)
  , redux_bank_withdraw_1 = redux_bank.withdraw(50)
  , redux_bank_withdraw_2 = redux_bank.withdraw(50)

console.log(redux_bank_withdraw_1.balance); // 50
console.log(redux_bank_withdraw_2.balance); // 50

var redux_bank_withdraw_3 = redux_bank_withdraw_1.withdraw(50)
console.log(redux_bank_withdraw_3)    		//  0

```




```javascript
// Bank has enviroment and users state -------------
var Bank = function(balance){
  this.balance = balance
}

Bank.prototype.withdraw = function(amount){
  this.balance = this.balance - amount
  return this.balance
}

// Redux Bank ---------------------------------------
var Redux_Bank = function(balance){
  this.balance = balance
}
// Instead of mutatting our balance,
// we create a new instance of Redux_Bank 
// and pass it to the update balance
Redux_Bank.prototype.withdraw = function(amount){
  return new Redux_Bank ( this.balance - amount)
}


// Imperitive Style
var bank 	   = new Bank(100)
  , withdraw_1 = bank.withdraw(50)
  , withdraw_2 = bank.withdraw(50)

// Calling withdraw with same arguments
// return different values
console.log(withdraw_1); // 50
console.log(withdraw_2); //  0



// Redux Style
var redux_bank 			  = new Redux_Bank(100)
  , redux_bank_withdraw_1 = redux_bank.withdraw(50)
  , redux_bank_withdraw_2 = redux_bank.withdraw(50)

console.log(redux_bank_withdraw_1.balance); // 50
console.log(redux_bank_withdraw_2.balance); // 50

var redux_bank_withdraw_3 = redux_bank_withdraw_1.withdraw(50)
console.log(redux_bank_withdraw_3.balance); // 0

```


# What can you expect here?

- How redux work?

- How you can use redux in real world example

- How you can use redux in real world example?

# Source 

-[Free Videos]()