## Bangboo Store ERD

``` mermaid
erDiagram
PRODUCT {
    int ProductID PK
    int Price
    str Size
    int Amount PK
}
CUSTOMER {
    str FirstName
    str LastName
    int PhoneNum
    alphanum Email
    alphanum Address 
    int CustomerID PK
}
SALE {
    int SaleID PK
    int CustomerID FK
    int ProductID FK
    int Amount FK
    alphanum DatePurchased
}
INVENTORY {
    str ProductName
    int ProductID PK
    int Amount FK
    int InStock
}

CUSTOMER ||..o{ SALE : makes
PRODUCT  ||..|{ SALE : is_sold_in
INVENTORY  ||..|| PRODUCT : is_tracked_in

```

## Documentation
### Customer
The Database stores personal information including name, email, phone number and address. However, when making transactions and public records, customers will have an ID specific to their info to be used in sales.

### Sales
Contains information of purchases by customers. It uses the customerID , productID, and number of products bought by the customer. To also keep confidentiality to the purchases of the customer, a SaleID will be given.

### Product
Product stores the many features of the product, including price, size and amount. Its ProductID makes it unique and is used for sales. 

### Inventory
This stores all information of products. It has the name of the product as well as the product ID from the product. It also has a category if a product is in stock. The amount of the product is found here, but is from the product section will all specifics of the product.