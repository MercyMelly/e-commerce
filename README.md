# E-Commerce Database Schema

This database schema provides a scalable and high-performance foundation for managing all aspects of an e-commerce platform—from product catalog and variants to inventory control and analytics. It is designed to enforce data integrity while supporting complex business operations with structured relationships and built-in logic.

---

## Core Structure

- **Products & Variants**  
  Multi-variant product system with support for color, size, and custom options.

- **Hierarchical Categories**  
  Categories are self-referencing to support parent-child relationships.

- **Attributes Management**  
  Flexible system for assigning attributes (e.g., material, dimensions) based on product type or category.

- **SKU-Level Inventory**  
  Tracks inventory at the most granular level—each product variant has a unique SKU.

---

## Data Integrity

- **Relational Constraints**
  - Foreign keys with `CASCADE`, `RESTRICT`, or `SET NULL` rules.
  - Unique constraints on SKUs and other key identifiers.

- **Validation Triggers**
  - Prevents invalid data entries (e.g., negative prices or stock levels).

- **Inventory Automation**
  - Triggers to auto-adjust inventory during order processing.

---

##  Performance Optimization

- **Strategic Indexing**
  - Indexes on all foreign key relationships.
  - Composite indexes for common query joins.
  - Full-text search on product names/descriptions.
  - Range indexes for price filtering and inventory status checks.

---

##  Business Logic

- **Stored Procedures**
  - Centralized logic for stock changes (purchase, returns, restocks).
  - Product variant retrieval with aggregation.

- **Catalog Views**
  - Pre-joined views for simplified data access (e.g., products + brands + categories).
  - Natural language search ready.

---

##  Analytics & Reporting

- **Inventory Dashboards**
  - Views with stock level classifications (low stock, out of stock, etc.).

- **Variation Overviews**
  - Human-readable listings of all options for each product.

- **Export-Ready Views**
  - Easily export catalog data including prices and images.

---

##  Sample Dataset

Includes optional seed data:
- Realistic product categories and items
- Variant examples (size, color, etc.)
- Inventory levels
- Search and reporting test cases

---
