```mermaid
graph TD
    %% App Structure
    subgraph Browser_Window [PharmaFlow v1.0 - Desktop Interface]
        direction TB
        
        subgraph Top_Navigation [Header Bar - Dark Blue]
            H1[fa:fa-clinic-medical PharmaFlow Logo]
            H2[fa:fa-user User: Pharmacist_01]
            H3[fa:fa-sign-out-alt Logout]
        end

        subgraph Sidebar_Menu [Navigation - Dark Blue]
            M1[fa:fa-chart-line Dashboard]
            M2[fa:fa-pills Inventory]
            M3[fa:fa-shopping-cart Sales POS]
            M4[fa:fa-cog Settings]
        end

        subgraph Main_Desktop [Active Work Area - Light Grey]
            subgraph Search_Area [Search & Selection - Gold]
                S1[fa:fa-barcode Scan Barcode]
                S2[fa:fa-search Search Medicine Name]
            end
            
            subgraph Cart_Area [Shopping Cart & Payment]
                C1[Item List: Aspirin x2, Paracetamol x1]
                C2[Total Amount: $25.50]
                C3[fa:fa-credit-card PAY NOW - GOLD BUTTON]
            end
        end
    end

    %% Connections
    M3 --> Main_Desktop
    S1 --> C1
    C3 --> H1

    %% Styling (Dark Blue & Gold)
    style Top_Navigation fill:#0d47a1,color:#fff,stroke:#000,stroke-width:2px
    style Sidebar_Menu fill:#1a237e,color:#fff,stroke:#000
    style Search_Area fill:#ffc107,color:#000,stroke:#e65100,stroke-width:2px
    style C3 fill:#ffc107,color:#000,stroke:#b8860b,stroke-width:3px
    style Main_Desktop fill:#f5f5f5,color:#000
    style H1 font-weight:bold,font-size:18px
```
## 🎨 UI/UX Design Strategy

### 1. Visual Identity
- **Primary Color (Dark Blue):** Chosen for the Header and Sidebar to evoke a sense of trust, stability, and professionalism in a medical environment.
- **Action Color (Gold):** Used for critical call-to-action buttons like "Pay Now" and "Search." This ensures the pharmacist's attention is immediately drawn to the most important tasks.

### 2. User Experience (UX) Goals
- **Efficiency:** The POS (Point of Sale) screen is optimized for high-speed transactions. Results appear instantly as the pharmacist types, reducing customer wait times.
- **Hierarchy:** Critical information, such as the "Total Amount," is centered and highlighted in Gold to prevent errors during busy hours.

### 3. Layout Breakdown
- **Sidebar:** Allows 1-click navigation between Inventory, Sales, and Reports.
- **Main Content:** A clean, high-contrast workspace that works well on both desktop monitors and tablets.
