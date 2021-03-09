# Procedure Crm_Offers_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Offer_Id](#offer_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` |The store, from which the products will be sold. When NULL, the store is unknown or N/A.|
|[Store_Id_Text](#store_id_text)|`nvarchar` `ML`|Name of the store|
|[Customer_Id](#customer_id)|`uniqueidentifier` |The customer to which the products are offered.|
|[Customer_Id_Text](#customer_id_text)|`nvarchar` `ML`|The name of the party|
|[Required_Delivery_Date](#required_delivery_date)|`date` |When not NULL, specifies required delivery date for all offer lines. When the lines contain different delivery dates, this is NULL.|
|[Valid_Till](#valid_till)|`datetime` |Last date when the offer is valid. NULL means the offer has no specific validity date|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document is issued. All amounts are in this currency|
|[Document_Currency_Id_Text](#document_currency_id_text)|`nvarchar` ||
|[Document_Currency_Sign](#document_currency_sign)|`nvarchar` |The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'.|
|[Accepted_On](#accepted_on)|`datetime` |The date on which the customer accepted the offer. NULL if the offer is not yet accepted or the date is unknown.|
|[Notes](#notes)|`nvarchar` ||
|[Total_Amount_Words](#total_amount_words)|`nvarchar` ||
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Way of payment. NULL means that no specific way of payment was offered|
|[Payment_Type_Id_Text](#payment_type_id_text)|`nvarchar` `ML`||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Responsible sales person. NULL when no sales person was assigned.|
|[Sales_Person_Id_Text](#sales_person_id_text)|`nvarchar` `ML`|The name of the party|

## Columns

### Offer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Valid_Till

| Property | Value |
| - | - |
|Type|datetime|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Accepted_On

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Amount_Words

| Property | Value |
| - | - |
|Type|nvarchar|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Type_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|


