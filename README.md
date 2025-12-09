# TECH-SHOP Database System

A comprehensive database management system for an electronics retail store, designed and implemented as part of the Database Systems course (CENG-1512), Faculty of Engineering, Department of Computer Engineering.

---

## 📋 Overview

TECH-SHOP is a relational database system built to manage all operational aspects of an electronics retail store, including:

- Inventory management
- Customer orders
- Employee tracking
- Sales invoicing

---

## 👥 Project Team

**Group #1**

- Nazar Nagi Zomrawi Mohammed 
- Anas Mohammed Abo Saeed "https://github.com/444032184"

_Course:_ Database Systems (CENG-1512)  
_Semester:_ Spring 2024

---

## 🎯 Key Features

- **Product Management:** Track products with details (price, quantity, brand, category, warehouse location)
- **Customer Management:** Store customer information and purchase history
- **Employee & Department Tracking:** Manage employees, departments, and managers hierarchically
- **Invoice System:** Generate detailed invoices (line items, discounts, VAT)
- **Vendor & Brand Management:** Track suppliers and brand relationships
- **Warehouse Management:** Monitor inventory across warehouses

---

## 🗄️ Database Schema

### Core Entities

- **PRODUCTS:** Catalog with pricing and inventory
- **CUSTOMER:** Contact and address information
- **EMPLOYEE:** Details and department assignments
- **INVOICE:** Transactions with payment info
- **INVOICE_ITEMS_LINE:** Individual invoice line items
- **BRANDS:** Brand information
- **CATEGARIES:** Product categories
- **VENDOR:** Supplier information
- **WAREHOUSE:** Storage location details
- **DEPARTMENT:** Organizational departments
- **MANAGERS:** Department managers

### Key Relationships

- Products link to vendors, warehouses, brands, categories
- Invoices connect customers, employees, products
- Employees belong to departments managed by managers
- Invoice line items resolve many-to-many between invoices & products

---

## 🔧 Technical Implementation

- **DBMS:** MySQL
- **Character Set:** UTF-8 (`utf8mb4`)
- **Schema Names:** `tech_shop` / `SKYLINE_SHOP`

### Key Constraints

- **Primary Keys:** Auto-incrementing IDs
- **Foreign Keys:** Referential integrity
- **Unique Constraints:** Email, brand, vendor, warehouse names
- **Check Constraints:**
  - Warehouse capacity ≥ 0
  - Product price and quantity ≥ 0
  - Discount ≥ 0 and ≠ 100
  - Product quantity in invoices ≥ 1
- **Default Values:**
  - Warehouse location: `AL-BAHA`
  - VAT: 15% (0.15)
  - Discount: 0

---

## 📊 Normalization Process

- **Issue Identified:** Many-to-many between ORDER and PRODUCT
- **Initial Solution:** Created INVOICE entity to link orders, products
- **Final Solution:** Added INVOICE_ITEMS_LINE junction table to resolve relationship, eliminate redundancy

---

## 💾 Sample SQL Operations

### Basic Operations

- **INSERT:** New customers, products, employees, invoices
- **UPDATE:** Change product prices, customer info, orders
- **DELETE:** Remove discontinued or inactive records

### Advanced Queries

- **JOINs:** Link products, invoices, customers, employees
- **Subqueries:** Analytical reporting
- **Aggregations:** Total sales, inventory, purchase history
- **GROUP BY:** Analyze sales by product, category, time period

---

## 📁 Project Files

- `RE_ERD_FINAL_PDF.pdf` – Final Entity-Relationship Diagram
- `SKYLINE_SHOP_SQL.sql` – Complete database schema (DDL)
- `QUERY FOR THE PROJECT.sql` – Sample queries & DML
- `DB Project Report.pdf` – Comprehensive documentation

---

## 🚀 Future Enhancements

**Proposed Improvements:**

- Employee state/entity for full-time, part-time, trainee
- Manager history (current/previous, department history)
- Specialized department tables (Shipment, Sales, HR, Security)

**Additional Entities:**

- **PAYMENT:** Support multiple payment methods
- **ORDER_SHIPMENTS:** Shipping/tracking info
- **Customer Support:** Online order management
- **Product Reviews/Ratings**

---

## 📚 Design Process

1. **Scenario Analysis:** Identify business requirements
2. **Entity Identification:** Extract entities, relationships
3. **Iterative ERD Design:** 7 iterations for schema refinement
4. **Normalization:** Eliminate redundancy, ensure integrity
5. **Constraint Definition:** Implement business rules
6. **Testing:** Validate with sample data & queries

---

## 🛠️ Technologies Used

- MySQL Workbench (Design & Modeling)
- MySQL Server (Implementation)
- SQL (DDL, DML, DQL)

---

## 📖 Reference

- *Database Systems: Design, Implementation and Management*, 11th Edition – Coronel & Morris, Cengage

---

## 📄 License

Developed for educational purposes (Database Systems course, Faculty of Engineering, Computer Engineering Department).

---

## 📧 Contact

For questions or collaboration, connect via LinkedIn.

---

_This system demonstrates practical database design, normalization, and SQL in a real-world retail scenario._
