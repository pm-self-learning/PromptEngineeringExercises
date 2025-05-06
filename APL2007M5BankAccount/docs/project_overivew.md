# BankAccount Application

## Overview
The BankAccount application is a simple C# program that models a bank account. It provides functionalities to manage account details, perform transactions, and calculate interest. This project is used to run prompts using GitHub Copilot and contains examples for prompt engineering.

## Features
- **Account Management**: Create a bank account with details such as account number, holder name, type, and opening date.
- **Transactions**:
  - Credit: Add funds to the account.
  - Debit: Withdraw funds from the account with balance validation.
  - Transfer: Transfer funds between accounts with restrictions for different account holders.
- **Balance Inquiry**: Check the current balance of the account.
- **Interest Calculation**: Calculate interest based on a given rate.
- **Statement Printing**: Print account details and recent transactions.

## Classes
### `BankAccount`
The `BankAccount` class represents a bank account and provides the following methods:
- `Credit(double amount)`: Adds the specified amount to the account balance.
- `Debit(double amount)`: Deducts the specified amount from the account balance if sufficient funds are available.
- `Transfer(BankAccount toAccount, double amount)`: Transfers the specified amount to another account with restrictions.
- `GetBalance()`: Returns the current account balance.
- `PrintStatement()`: Prints the account statement.
- `CalculateInterest(double interestRate)`: Calculates interest based on the current balance and the provided interest rate.

## Usage
1. Clone the repository.
2. Navigate to the `APL2007M5BankAccount` project directory.
3. Build and run the project using your preferred C# compiler or IDE.

## Example
```csharp
using System;
using BankAccountApp;

class Program
{
    static void Main(string[] args)
    {
        var account1 = new BankAccount("123456", 1000, "John Doe", "Savings", DateTime.Now);
        var account2 = new BankAccount("654321", 500, "Jane Doe", "Savings", DateTime.Now);

        account1.Credit(200);
        account1.Debit(100);
        account1.Transfer(account2, 300);

        Console.WriteLine($"Account 1 Balance: {account1.GetBalance()}");
        Console.WriteLine($"Account 2 Balance: {account2.GetBalance()}");
    }
}
```

## Testing
Unit tests for the `BankAccount` class are located in the `BankAccount.UnitTests` project. To run the tests:
1. Navigate to the `BankAccount.UnitTests` directory.
2. Build and run the tests using your preferred C# testing framework.

## License
This project is licensed under the MIT License.