# Table Crm_Offers

Offers (quotes) for sales of products. Can contain variants and choice groups. The user can select some approved lines and generate Sales Order. Entity: Crm_Offers

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Offer_Id](#offer_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Deal_Id](#deal_id)|`uniqueidentifier` |The opportunity (deal) on which this offer is based.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store, from which the products will be sold. When NULL, the store is unknown or N/A.|
|[Customer_Id](#customer_id)|`uniqueidentifier` |The customer to which the products are offered.|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |The price list, based on which the prices are selected. Initially copied from the definition of the Customer.|
|[Required_Delivery_Date](#required_delivery_date)|`date` |When not NULL, specifies required delivery date for all offer lines. When the lines contain different delivery dates, this is NULL.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document is issued. All amounts are in this currency|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Way of payment. NULL means that no specific way of payment was offered|
|[Payment_Due_Date](#payment_due_date)|`datetime` |The last term for payment|
|[Valid_Till](#valid_till)|`datetime` |Last date when the offer is valid. NULL means the offer has no specific validity date|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Responsible sales person. NULL when no sales person was assigned.|
|[Accepted_On](#accepted_on)|`datetime` |The date on which the customer accepted the offer. NULL if the offer is not yet accepted or the date is unknown.|
|[Recipient_Person_Id](#recipient_person_id)|`uniqueidentifier` |The offer recipient. It should be employee of the customer. NULL means that there is no default recipient or he/she is unknown|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Offer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Valid_Till

| Property | Value |
| - | - |
|Type|datetime|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Accepted_On

| Property | Value |
| - | - |
|Type|datetime|

### Recipient_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


