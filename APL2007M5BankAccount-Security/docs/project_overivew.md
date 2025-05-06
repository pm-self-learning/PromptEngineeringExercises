# BankAccount Security Application

## Overview
The BankAccount Security application is a C# program that models a bank account with a focus on security. It provides functionalities to manage account details, perform transactions, and calculate interest while adhering to security best practices. This project is used to demonstrate security-focused prompt engineering examples.

## Features
- **Account Management**: Create a bank account with details such as account number, holder name, type, and opening date.
- **Transactions**:
  - Credit: Add funds to the account.
  - Debit: Withdraw funds from the account with balance validation.
  - Transfer: Transfer funds between accounts with restrictions for different account holders.
- **Balance Inquiry**: Check the current balance of the account.
- **Interest Calculation**: Calculate interest based on a given rate.
- **Statement Printing**: Print account details and recent transactions.

## Security Enhancements
- **Authentication and Authorization**: Implement robust mechanisms to protect against unauthorized access.
- **Data Protection**: Encrypt sensitive data both at rest and in transit.
- **Error Handling**: Securely handle exceptions to avoid exposing sensitive information.
- **Dependency Management**: Ensure third-party libraries are up-to-date and free from vulnerabilities.
- **Security Testing**: Conduct thorough security testing to identify and mitigate vulnerabilities.

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
1. Navigate to the `APL2007M5BankAccount-Security` project directory.
2. Build and run the project using your preferred C# compiler or IDE.

## Testing
Unit tests for the `BankAccount` class are located in the `BankAccount.UnitTests` project. To run the tests:
1. Navigate to the `BankAccount.UnitTests` directory.
2. Build and run the tests using your preferred C# testing framework.

## Next Steps

- Refer to the [`exercise.md`](../docs/exercise.md) file for hands-on exercise.