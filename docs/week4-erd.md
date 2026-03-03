```mermaid
graph TD
    %% Database Tables grouped by Role/Theme
    subgraph User_Management_System [USERS & PERMISSIONS - Dark Blue]
        U[fa:fa-id-card USERS TABLE <br/> ------------------ <br/> user_id PK <br/> username <br/> password <br/> role]
    end

    subgraph Inventory_System [MEDICINES & STOCK - Gold]
        M[fa:fa-pills MEDICINES TABLE <br/> ------------------ <br/> med_id PK <br/> name <br/> price <br/> stock <br/> expiry_date]
        SP[fa:fa-industry SUPPLIERS TABLE <br/> ------------------ <br/> supplier_id PK <br/> company_name <br/> phone]
    end

    subgraph Transaction_System [SALES & LOGS - Dark Blue]
        S[fa:fa-file-invoice-dollar SALES TABLE <br/> ------------------ <br/> sale_id PK <br/> med_id FK <br/> user_id FK <br/> quantity <br/> total_price]
    end

    %% Relationships (Data Flow)
    U ==>|Tracks Seller| S
    M ==>|Updates Quantity| S
    SP ==>|Restocks| M

    %% Styling (2-haftadagi kabi ranglar)
    
    %% Dark Blue Sections (Users & Sales)
    style User_Management_System fill:#1a237e,color:#fff,stroke:#0d47a1,stroke-width:2px
    style Transaction_System fill:#1a237e,color:#fff,stroke:#0d47a1,stroke-width:2px
    style U fill:#0d47a1,color:#fff,stroke:#fff
    style S fill:#0d47a1,color:#fff,stroke:#fff

    %% Gold Section (Medicines & Suppliers)
    style Inventory_System fill:#ffc107,color:#000,stroke:#e65100,stroke-width:2px
    style M fill:#fff8e1,color:#000,stroke:#e65100
    style SP fill:#fff8e1,color:#000,stroke:#e65100
```
## Database Architecture - Week 4

The **PharmaFlow** database is structured into three main modules, similar to our business process flow:

1. **User Management (Dark Blue):** Handles authentication and authorization. It records which employee (Admin/Pharmacist) is using the system.
2. **Inventory System (Gold):** Manages the products. It links each medicine to its supplier and tracks stock levels automatically.
3. **Transaction System (Dark Blue):** The core of the POS. Every sale is linked to a specific medicine and a specific user to ensure accountability.

**Relationships:**
- **Primary Keys (PK):** Unique IDs for each entry.
- **Foreign Keys (FK):** Used to create relationships between tables (e.g., Sales table links to both Medicines and Users).
