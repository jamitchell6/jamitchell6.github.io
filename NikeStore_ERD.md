'''mermaid
erDiagram
    PRODUCT ||--{ ORDER : places
    }
    CUSTOMER ||--{
    string name
    string custNumber
    string sector
    }
    SALE {
    int orderNumber
    string deliveryAddress
    }
    INVENTORY {
    int quantity
    float pricePerUnit
    }

    PRODUCT ||--|{shoes :  contains
    CUSTOMER ||--|{buyer : contains
    SALE ||--|{order : contains
    INVENTORY ||--{quantity

    There is shoes as the product to buy. The sale is the order of the shoes. Inventory is the amount of shoes left that weren't brought by customers.
