# Procedure Crm_Sales_Orders_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Payment_Account_Name](#payment_account_name)|`nvarchar` `ML`||
|[Customer_Id](#customer_id)|`uniqueidentifier` |The primary customer, which placed the sales order|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |The price list to be used for determining product prices in the lines|
|[Payment_Due_Date](#payment_due_date)|`datetime` |The last term for the payment of the sales order|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|
|[Required_Delivery_Date](#required_delivery_date)|`date` |The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to issue the sales order. NULL means that there is no store associated with the sales order or there are different stores for some of the lines|
|[Lines_Total](#lines_total)|`decimal(0, 0)` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, the payment account, where the payment is expected. NULL=no expectation for account|
|[Notes](#notes)|`nvarchar` ||
|[Document_Currency_Sign](#document_currency_sign)|`nvarchar` |The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'.|
|[Document_Currency_Id_Text](#document_currency_id_text)|`nvarchar` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the document; e.g. the currency of the amounts in the document|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type.|
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar` |Reference number of the customer's purchase order|
|[Amount_To_Pay](#amount_to_pay)|`decimal(0, 0)` ||
|[Total_Amount_Words](#total_amount_words)|`nvarchar` ||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` `PK`||
|[Return_For_Sales_Order_Id](#return_for_sales_order_id)|`uniqueidentifier` |When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document|
|[Price_List_Id_Text](#price_list_id_text)|`nvarchar` ||
|[Dealer_Id_Text](#dealer_id_text)|`nvarchar` ||
|[Dealer_Id](#dealer_id)|`uniqueidentifier` |The external dealer, associated with the sales order|
|[Sales_Person_Id_Text](#sales_person_id_text)|`nvarchar` `ML`|The name of the party|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Internal company sales person|
|[Store_Id_Text](#store_id_text)|`nvarchar` `ML`|Name of the store|
|[Ship_To_Party_Contact_Mechanism_Id_Text](#ship_to_party_contact_mechanism_id_text)|`nvarchar` ||
|[Ship_To_Party_Contact_Mechanism_Id](#ship_to_party_contact_mechanism_id)|`uniqueidentifier` |The contact mechanism (address) to whih to ship the sales order|
|[Customer_Id_Text](#customer_id_text)|`nvarchar` `ML`|The name of the party|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Payment_Type_Name](#payment_type_name)|`nvarchar` `ML`||
|[Return_For_Invoice_Id](#return_for_invoice_id)|`uniqueidentifier` |When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document|

## Columns

### Payment_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lines_Total

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_To_Pay

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Amount_Words

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Return_For_Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Dealer_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Ship_To_Party_Contact_Mechanism_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Ship_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Return_For_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


