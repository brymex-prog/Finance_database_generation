# Finance Database Design and Implementation

A relational finance database project built using SQLite and Python to simulate a realistic personal banking and investment management system.

## Overview

This project demonstrates advanced relational database design concepts using a finance-based dataset. The database models real-world financial relationships between customers, accounts, transactions, and investments.

The project includes:

- Relational schema design
- Primary and foreign key implementation
- Composite primary keys
- Referential integrity constraints
- Synthetic financial data generation
- Missing and duplicate data simulation
- Ethical data generation practices

---

## Technologies Used

- Python
- SQLite
- Faker Library
- Google Colab

---

## Database Structure

The database contains 6 interconnected tables:

### 1. Customers
Stores customer information.

### 2. Accounts
Stores financial account details including:
- Savings accounts
- Checking accounts
- Investment accounts

### 3. AccountHolders
Many-to-many relationship table connecting customers and accounts.

Composite Key:
- `(customer_id, account_id)`

### 4. Transactions
Stores all financial transactions.

Composite Key:
- `(transaction_id, account_id)`

### 5. TransactionCategories
Categorises transactions into groups such as:
- Income
- Expense
- Transfer

### 6. Investments
Stores customer investment records and risk levels.

---

## Database Relationships

- Customers → AccountHolders (1:M)
- Accounts → AccountHolders (1:M)
- Accounts → Transactions (1:M)
- Transactions → TransactionCategories (M:1)
- Customers → Investments (1:M)

---

## Features

- Fully normalised relational schema
- Composite primary keys
- Foreign key constraints
- CHECK constraints
- UNIQUE constraints
- Realistic synthetic financial data
- Support for joint accounts
- Multiple currencies (GBP, USD, EUR)
- Intentional missing and duplicate data simulation

---

## Synthetic Data Generation

Data was generated using Python and Faker.

### Dataset Includes

- 500 Customers
- 700 Accounts
- 7,000–10,000 Transactions
- 400 Investments
- 5 Transaction Categories

### Realism Features

- NULL email values (~3%)
- Duplicate email records
- Random account balances
- Multi-year transaction history
- Variable investment risk levels

---

## Data Integrity Constraints

The database enforces:

- PRIMARY KEY constraints
- FOREIGN KEY constraints
- Composite keys
- UNIQUE constraints
- CHECK constraints
- Referential integrity

---

## Ethical Considerations

All data used in this project is fully synthetic.

No real personal or financial data has been used.

The project follows ethical data generation and privacy protection practices.

---

## Possible Analytical Applications

This database supports:

- Spending analysis
- Customer portfolio analysis
- Income vs expense reporting
- Investment risk analysis
- Transaction frequency analysis
- Fraud detection research
- Predictive analytics experimentation

---

## Project Purpose

This project was created as part of a database and data science learning exercise to demonstrate practical understanding of:

- Relational database systems
- Database normalisation
- Financial data modelling
- SQL constraints
- Synthetic data engineering

---

## Author

Ibrahim Abdulsalam

---

## License

This project is licensed under the MIT License.
