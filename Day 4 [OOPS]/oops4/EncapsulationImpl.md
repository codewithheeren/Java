## OOPS - Encapsulation Implementation 

### BankAccount.java

```java
/**
 * Pojo Class
 * By using private fields and providing public getter and setter methods, 
 * you control how the data is accessed and modified. 
 * For example, in the BankAccount class, you can ensure that the balance 
 * is never set directly and can only be modified through the deposit and
 *  withdraw methods which contain business logic for validation.
 * @author Heeren
 * @version 1.0
 */

package com.codewithheeren.java.oops4;

public class BankAccount {
	private String accountNumber;
	private String accountHolderName;
	private double balance;

	public BankAccount(String accountNumber, String accountHolderName, double initialBalance) {
		this.accountNumber = accountNumber;
		this.accountHolderName = accountHolderName;
		this.balance = initialBalance;
	}

	public String getAccountNumber() {
		return accountNumber;
	}

	public void setAccountNumber(String accountNumber) {
		this.accountNumber = accountNumber;
	}

	public String getAccountHolderName() {
		return accountHolderName;
	}

	public void setAccountHolderName(String accountHolderName) {
		this.accountHolderName = accountHolderName;
	}

	public double getBalance() {
		return balance;
	}

	public void deposit(double amount) {
		if (amount > 0) {
			balance += amount;
		} else {
			System.out.println("Invalid deposit amount.");
		}
	}

	public void withdraw(double amount) {
		if (amount > 0 && amount <= balance) {
			balance -= amount;
		} else {
			System.out.println("Invalid withdrawal amount.");
		}
	}
}

```
---

### BankApp.java
```java
package com.codewithheeren.java.oops4;
public class BankApp {
    public static void main(String[] args) {
        BankAccount account = new BankAccount("123456789", "John Doe", 500.0);

        System.out.println("Account Holder: " + account.getAccountHolderName());
        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Initial Balance: $" + account.getBalance());

        // Perform some transactions
        account.deposit(150.0);
        System.out.println("Balance after deposit: $" + account.getBalance());

        account.withdraw(100.0);
        System.out.println("Balance after withdrawal: $" + account.getBalance());

        // Attempt to withdraw an invalid amount
        account.withdraw(600.0);
    }
}

```
---
