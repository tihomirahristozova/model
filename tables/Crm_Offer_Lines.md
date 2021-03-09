# Table Crm_Offer_Lines

Detail records (lines) of Offers. Entity: Crm_Offer_Lines

## Owner Tables Hierarchy

* [Crm_Offers](Crm_Offers.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` ||
|[Is_Selected](#is_selected)|`bit` |1 when the line is selected for further processing (ordering), 0 otherwise.|
|[Variant](#variant)|`nvarchar(60)` |Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.|
|[Product_Id](#product_id)|`uniqueidentifier` |The offered product.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The description of the offered product. Initially copied from the name of the offered product.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity offered.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the offered product. It is specified in the measurement unit of Quantity.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Offer_Line_Id](#offer_line_id)|`uniqueidentifier` `PK`||
|[Notes](#notes)|`nvarchar(254)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` Readonly|The equivalent of Quantity in the base measurement unit of the Product|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Not NULL, when the product is selected using a coding system code.|
|[Choice_Group_Name](#choice_group_name)|`nvarchar(60)` |Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |Operator defined discount percentage, specified for this line.|
|[Delivery_Term_Days](#delivery_term_days)|`int` |Delivery term in days. When Required Delivery Date is specified (not NULL), it takes precedence and this is ignored.|
|[Row_Version](#row_version)|`timestamp` ||
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` |The discount percentage, applied through the standard discount policy.|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |When not NULL, contains the discount policy selected for this line.|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` |Not NULL when the price has been selected from the list of valid standard prices|
|[Offer_Id](#offer_id)|`uniqueidentifier` ||
|[Required_Delivery_Date](#required_delivery_date)|`date` |Date, when the delivery is required. Alternative to Delivery Term Days. When NULL, Delivery Term Days is used.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Is_Selected

| Property | Value |
| - | - |
|Type|bit|

### Variant

| Property | Value |
| - | - |
|Type|nvarchar(60)|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Offer_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Choice_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(60)|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Delivery_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Offer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


