# Restaurant Billing System

## Overview
The Restaurant Billing System is a command-line application designed to streamline the invoice generation and management process for Keyur's Restaurant. This C-based program provides a digital solution for creating, storing, retrieving, and organizing customer bills, replacing traditional paper-based methods with an efficient electronic system.

## Features
- **Invoice Generation**: Create detailed invoices with customer information, items ordered, quantities, and prices.
- **Bill Records**: Maintain a database of all transactions for record-keeping and future reference.
- **Invoice Retrieval**: Search for specific invoices by customer name.
- **Reporting**: View all previously generated invoices to track sales history.
- **Automatic Calculations**: The system automatically calculates subtotals, discounts, taxes, and final amounts.

## Technical Implementation
The program is built using C and implements the following core components:

### Data Structures
- `struct items`: Stores information about individual items including name, price, and quantity.
- `struct orders`: Maintains complete order details including customer name, date, number of items, and an array of item structures.

### File Operations
- Invoices are stored in a binary file format (`RestaurantBill.dat`) using file I/O operations.
- Data persistence is maintained between program executions.

### Key Functions
- `generateBillHeader()`: Formats and displays the invoice header with restaurant name, customer details, and date.
- `generateBillBody()`: Lists individual items with their quantities and calculated prices.
- `generateBillFooter()`: Displays financial calculations including subtotal, discounts (10%), taxes (CGST & SGST at 5% each), and the grand total.

## User Interface
The program offers a simple menu-driven interface with four main options:
1. Generate Invoice: Create a new bill for a customer
2. Show all Invoices: Display all stored invoices
3. Search Invoice: Find and display a specific invoice by customer name
4. Exit: Close the application

## Financial Logic
The system implements the following business rules:
- 10% discount on the subtotal
- 5% CGST (Central Goods and Services Tax)
- 5% SGST (State Goods and Services Tax)
- Final amount calculated as: (Subtotal - Discount) + CGST + SGST

## Usage Instructions
1. Compile the program using a C compiler such as GCC:
   ```bash
   gcc restaurant.c -o restaurant
   ```
2. Run the executable:
   ```bash
   ./restaurant
   ```
3. Follow the on-screen prompts to navigate through the system's functions.

## System Requirements
- C compiler (GCC recommended)
- Standard C libraries (stdio.h, string.h, stdlib.h)
- Terminal/Command prompt environment

## Limitations and Future Improvements
- The current version uses a fixed file format that doesn't support modifications to existing invoices.
- The system is limited to 50 items per order and 20 characters per item name.
- Future versions could include:
  - User authentication
  - Enhanced search capabilities (by date, amount, etc.)
  - Data export to common formats (CSV, PDF)
  - Graphical user interface
  - Inventory integration

## Developer Information
This application was developed by Keyur as a practical solution for restaurant bill management, demonstrating fundamental programming concepts including:
- Structured programming
- File I/O operations
- Dynamic memory allocation
- Data structures
- User interface design

For questions or further development, please contact the project maintainer.
