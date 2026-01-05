# Virtual Store Application — Java (Programming 3 Project)

This repository contains the **MAXISO Virtual Store Application**, a console-based shopping system developed as a **Programming 3 team project** at **Dawson College**.

The project simulates a fully functional virtual store where users can browse products, manage a shopping cart, register/login, apply coupons, and complete purchases — all while demonstrating **advanced object-oriented design, unit testing, and clean separation of concerns**.

> **Important:**  
> This project must be run from the `javaproject/merch` directory for file paths (CSV storage) to work correctly.

## Project Overview
The application supports both **guest users** and **registered users**, with registered users gaining access to:
- Shopping cart functionality
- Loyalty points
- Coupon discounts

All data (products, users, coupons) is stored in **CSV files**, making the system lightweight, transparent, and easy to test or modify.

## Concepts Demonstrated
This project showcases the following key programming concepts:

- **Object-Oriented Programming (OOP)**  
  - Encapsulation, inheritance, polymorphism  
  - Clear domain modeling (Users, Products, Coupons, Cart)

- **Programming to Interfaces**  
  - Display layer abstractions  
  - Filtering and sorting strategies

- **Separation of Concerns**  
  - Business logic layer  
  - Data access layer  
  - Display/UI layer

- **Java Collections & Data Structures**  
  - Lists for product catalogs and carts  
  - Iteration, filtering, sorting

- **File-Based Persistence (CSV)**  
  - Users, products, and coupons loaded from CSV files  
  - Simple, human-readable storage format

- **Unit Testing (JUnit)**  
  - Full test coverage of core logic  
  - Ensures correctness and regression safety

## Testing & Quality
The project is **fully unit tested** using **JUnit**.

**Test Results:**
```
[INFO] Tests run: 48, Failures: 0, Errors: 0, Skipped: 0
[INFO] BUILD SUCCESS
```

## Tech Stack
- **Language:** Java  
- **Build Tool:** Maven  
- **Testing:** JUnit  
- **Persistence:** CSV files  
- **Architecture:** Layered (Business / Data / Display)

## Project Structure
```
VirtualStore-Application-Project--Java-3/
│
├── README.md
└── javaproject/
    └── merch/
        ├── csv/
        │   ├── Users.csv
        │   ├── Coupons.csv
        │   ├── Electronics.csv
        │   ├── Figurines.csv
        │   └── Plushies.csv
        │
        ├── src/
        │   ├── main/java/maxiso/
        │   │   ├── businesslayer/
        │   │   ├── datalayer/merch/
        │   │   └── displaylayer/
        │   │       └── App.java
        │   │
        │   └── test/java/maxiso/
        │   │   └── (JUnit tests)
        │
        └── pom.xml
```

## How to Run Locally

1) Clone the repository
```bash
git clone https://github.com/artembrandt03/VirtualStore-Application-Project--Java-3.git
cd VirtualStore-Application-Project--Java-3
```

3) Navigate to the correct directory
```bash
cd javaproject/merch
```

> **This step is required**  
> CSV file paths are relative to this directory.

3) Compile and run the application
```bash
mvn clean compile
mvn exec:java -Dexec.mainClass="maxiso.App"
```

### Test Credentials

You can log in using the following test account:

- **Username:** `TestUser`  
- **Password:** `Test123`

Or feel free to **register a new account directly from the app** — it will be saved automatically to `Users.csv`.

## Demo in Browser (GitHub Codespaces)

1) Click **Code** → **Codespaces** → **Create codespace on main**
2) Wait for the dev container to finish setting up (it auto-compiles)
3) Run:

```bash
cd javaproject/merch
mvn test
mvn -q exec:java -Dexec.mainClass="maxiso.App"
```

## Features Overview

### User Management
- Guest mode
- Registered users with login & registration
- Loyalty points tracking

### Product Browsing
- Categories: Figurines, Plushies, Electronics, All Products
- Filtering by price range and collection
- Sorting by ascending or descending price
- One-product-per-page navigation

### Shopping Cart
- Add and remove items
- Navigate through cart items
- Apply coupons during checkout
- Clear cart after purchase

## Video Showcase
(low quality due to video compression)

https://github.com/user-attachments/assets/5850620b-7edb-47a5-97bf-ff6d10488116

## Contributors

- **Artem Brandt**
- **Haider Ahmed**
- **Angie Fu**