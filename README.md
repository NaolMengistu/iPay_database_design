# Mobile Payment Service Database

This repository contains the database design for a mobile payment service similar to platforms like Cash App or Venmo. The database was developed as part of my bachelor thesis and is designed to support the backend of a mobile payment platform, facilitating user account management, peer-to-peer transactions, service purchases, and more.

## Overview

The database is built using **MySQL** and adheres to relational database design principles, including ACID compliance and normalization up to the Third Normal Form (3NF). The design emphasizes scalability, consistency, and maintainability while ensuring data security and integrity.

### Features
- **User Management**: Tracks user profiles, credentials, and balances.
- **Transactions**: Manages peer-to-peer payments, service purchases, and transaction statuses.
- **Services**: Supports tracking of platform-based services and purchases.
- **Audit and Tracking**: Logs database changes for transparency and troubleshooting.
- **Modular Design**: Ensures scalability and adaptability for future expansions.

## Files

### 1. `iPay database.mwb`
The MySQL Workbench file (`.mwb`) contains the full database schema, including all entities, attributes, relationships, and constraints. Open this file in MySQL Workbench for a visual representation of the schema.

### 2. `iPay database.sql`
This SQL file contains the full script to create the database schema. It is suitable for direct import into a MySQL database instance.

#### How to Use `iPay database.sql`
1. Open your MySQL client or database management tool.
2. Import the `iPay database.sql` file.
   - Example using MySQL command line:
     ```bash
     mysql -u [username] -p [database_name] < iPay database.sql
     ```
3. Verify that the schema is created and ready for use.

## Database Schema

The database schema is designed to support the following key entities and relationships:

1. **Person**: Stores personal information like name, email, phone number, and associated addresses.
2. **Address**: Captures user and service provider addresses.
3. **User**: Links personal profiles to account details and balances.
4. **Account**: Tracks internal and external account numbers.
5. **Card**: Stores card details, including PAN, expiration date, and CVV.
6. **Transaction**: Manages money transfers, service purchases, and related metadata.
7. **Service**: Tracks services offered by providers and purchased by users.
8. **Fee**: Defines and applies transaction fees based on transaction types.
9. **Currency**: Supports multi-currency transactions.
10. **Status**: Tracks the state of transactions (e.g., pending, completed, failed).
11. **Tracker**: Logs database changes for auditing purposes.

### Key Design Highlights
- **Normalization**: The database schema follows the First (1NF), Second (2NF), and Third Normal Forms (3NF) to minimize redundancy and maintain consistency.
- **ACID Compliance**: Ensures atomicity, consistency, isolation, and durability for reliable transactions.
- **Scalability**: Designed to accommodate future expansions and additional features.

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Naola/iPay_database_design.git
2. Open iPay database.mwb in MySQL Workbench to view the schema, or import iPay database.sql into your MySQL instance.
