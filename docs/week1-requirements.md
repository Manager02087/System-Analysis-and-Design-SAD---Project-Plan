# Week 1: Requirements Analysis - PharmaFlow

## 1. Introduction
The goal of this phase is to define the boundaries of the PharmaFlow system and identify the specific needs of its users.

## 2. Functional Requirements (FR)
These requirements define the specific behaviors and functions of the system.

| ID | Requirement Name | Description |
|:---|:---|:---|
| **FR-01** | **Inventory Control** | The system must allow users to add, update, and delete medicine records (Name, Batch, Price, Stock). |
| **FR-02** | **Expiration Tracking** | The system must automatically highlight medicines that are within 3 months of their expiry date. |
| **FR-03** | **Sales Processing** | The system must process transactions via barcode scanning and calculate totals/taxes. |
| **FR-04** | **Report Generation** | The system must generate daily and monthly sales reports in PDF/Excel formats. |
| **FR-05** | **User Management** | Admins must be able to create accounts for Pharmacists and assign permissions. |

## 3. Non-Functional Requirements (NFR)
These define the quality attributes of the system.

* **Usability:** The interface should be intuitive enough for a pharmacist to learn within 30 minutes.
* **Performance:** All search queries must return results in less than 1 second.
* **Security:** Passwords must be encrypted using SHA-256.
* **Availability:** The system should be accessible 99.9% of the time.

## 4. User Personas
1.  **Admin (Owner):** Needs full visibility of profits and inventory.
2.  **Pharmacist:** Needs a fast, lag-free interface to serve customers quickly.
3.  **Stock Manager:** Needs accurate data to avoid overstocking or stockouts.

---
*Last Updated: February 12, 2026*