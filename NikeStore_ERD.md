```mermaid
erDiagram
    PRODUCT ||--o{ INVENTORY : "has"
    PRODUCT {
        string model_name
        string collection
        float price
        string size
        string colorway
    }
    
    CUSTOMER ||--o{ SALES : "makes"
    CUSTOMER {
        int customer_id
        string name
        string email
        string phone
        string address
    }
    
    SALES }|--|| PRODUCT : "includes"
    SALES {
        int sale_id
        int customer_id
        int product_id
        date sale_date
        float total_amount
        int quantity
    }
    
    INVENTORY {
        int product_id
        int stock_level
        string location
        date last_updated
    }


All 4 categories feed off each other as the customers come fore the product and with supply and demand the inventory will be be stocked appropriately and maybe prices will be adjusted depending on how poorly or well a productis doing in the sales category 
