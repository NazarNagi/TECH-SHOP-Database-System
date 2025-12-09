# TECH-SHOP-Database-System
A comprehensive database management system for an electronics retail store, designed and implemented as part of the Database Systems course (CENG-1512) at the Faculty of Engineering, Department of Computer Engineering.

📋 Project Overview
TECH-SHOP is a relational database system that manages all aspects of an electronics retail store operation, including inventory management, customer orders, employee tracking, and sales invoicing. The system was developed through an iterative design process, evolving through 7 major ERD iterations to achieve optimal database normalization and structure.
#👥 Project Team
Group #1

Nazar Nagi Zomrawi Mohammed (ID: 444032185)
Anas Mohammed Abo Saeed (ID: 444032184)

Course: Database Systems (CENG-1512)
Semester: Spring 2024
#🎯 Key Features

Product Management: Track products with detailed information including price, quantity, brand, category, and warehouse location
Customer Management: Store customer information and purchase history
Employee & Department Tracking: Manage employees, departments, and managers with hierarchical relationships
Invoice System: Generate detailed invoices with line items, discounts, and VAT calculations
Vendor & Brand Management: Track product suppliers and brand relationships
Warehouse Management: Monitor inventory across multiple warehouse locations

#🗄️ Database Schema
Core Entities

PRODUCTS - Product catalog with pricing and inventory
CUSTOMER - Customer contact and address information
EMPLOYEE - Employee details and department assignments
INVOICE - Sales transactions with payment information
INVOICE_ITEMS_LINE - Individual line items for each invoice
BRANDS - Product brand information
CATEGARIES - Product categories
VENDOR - Supplier information
WAREHOUSE - Storage location details
DEPARTMENT - Organizational departments
MANAGERS - Department managers

Key Relationships

Products are linked to vendors, warehouses, brands, and categories
Invoices connect customers, employees, and products
Employees belong to departments managed by specific managers
Invoice line items resolve the many-to-many relationship between invoices and products

#🔧 Technical Implementation
Database Engine

DBMS: MySQL
Character Set: UTF-8 (utf8mb4)
Schema Name: tech_shop / SKYLINE_SHOP

Key Constraints

Primary Keys: Auto-incrementing IDs for all entities
Foreign Keys: Referential integrity across all relationships
Unique Constraints: Email addresses, brand names, vendor names, warehouse names
Check Constraints:

Warehouse capacity ≥ 0
Product price and quantity ≥ 0
Discount ≥ 0 and ≠ 100
Product quantity in invoices ≥ 1


Default Values:

Warehouse location: 'AL-BAHA'
VAT: 15% (0.15)
Discount: 0



#📊 Normalization Process
The database underwent a comprehensive normalization process to eliminate redundancy and ensure data integrity:

Issue Identified: Many-to-many relationship between ORDER and PRODUCT entities
Initial Solution: Created INVOICE entity to link orders and products
Final Solution: Implemented INVOICE_ITEMS_LINE junction table to properly resolve the relationship while eliminating data redundancy

#💾 Sample SQL Operations
Basic Operations

INSERT: Add new customers, products, employees, and invoices
UPDATE: Modify product prices, customer information, and order statuses
DELETE: Remove discontinued products or inactive records

Advanced Queries

JOIN Operations: Complex queries linking products, invoices, customers, and employees
Subqueries: Nested queries for analytical reporting
Aggregations: Calculate total sales, inventory summaries, and customer purchase history
GROUP BY: Analyze sales by product, category, or time period

#📁 Project Files

RE_ERD_FINAL_PDF.pdf - Final Entity-Relationship Diagram
SKYLINE_SHOP_SQL.sql - Complete database schema DDL statements
QUERY FOR THE PROJECT.sql - Sample queries and DML operations
DB Project Report.pdf - Comprehensive project documentation

#🚀 Future Enhancements
Proposed Improvements

Employee State Management: Add entity to track employment types (full-time, part-time, trainee)
Manager History: Track current and previous managers with department history
Department Specialization: Create specialized tables for different departments (Shipment, Sales, HR, Security)
Additional Entities:

PAYMENT - Multiple payment method support
ORDER_SHIPMENTS - Shipping and tracking information
Customer Support System - Online order management
Product Reviews and Ratings



#📚 Design Process
The project followed a systematic database design methodology:

Scenario Analysis: Identified real-world business requirements
Entity Identification: Extracted entities and relationships from the scenario
Iterative ERD Design: Created 7 iterations of the ERD to refine the schema
Normalization: Applied normalization principles to eliminate redundancy
Constraint Definition: Implemented business rules through database constraints
Testing: Validated with sample data and queries

#🛠️ Technologies Used

MySQL Workbench (Database Design & Modeling)
MySQL Server (Database Implementation)
SQL (DDL, DML, DQL operations)

#📖 Reference
Database Systems: Design, Implementation and Management, 11th Edition - Coronel and Morris, Cengage

#📄 License
This project was developed for educational purposes as part of the Database Systems course at the Faculty of Engineering, Department of Computer Engineering.
#📧 Contact
For questions or collaboration opportunities, please reach out via LinkedIn.

This database system demonstrates practical application of database design principles, normalization techniques, and SQL implementation in a real-world retail management scenario.
