# Table Crm_Customer_Products

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products

## Owner Tables Hierarchy

* [Crm_Customers](Crm_Customers.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Product_Id](#customer_product_id)|`uniqueidentifier` `PK`|Customer Product listing|
|[Customer_Id](#customer_id)|`uniqueidentifier` |Customer, for which the product is listed|
|[Company_Division_Id](#company_division_id)|`uniqueidentifier` |When the customer is a company, denotes the division for which the product is listed. NULL when the customer is not a company or when the listing is not division specific|
|[Company_Location_Id](#company_location_id)|`uniqueidentifier` |When the customer is a company, denotes the location for which the product is listed. NULL when the customer is not a company or when the listing is not location specific|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is listed for the customer|
|[From_Date](#from_date)|`date` |The initial date of the listing. NULL when the initial date is unknown|
|[To_Date](#to_date)|`date` |The final date of the listing. NULL when the final date is unknown|
|[Notes](#notes)|`nvarchar(254)` |Notes for the listing|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Customer_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|date|

### To_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


