# Procedure Crm_Offers_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Picture_No](#picture_no)|`int` |Unique picture number within the product. Also used for sorting|
|[Line_No](#line_no)|`int` ||
|[Is_Selected](#is_selected)|`bit` |1 when the line is selected for further processing (ordering), 0 otherwise.|
|[Variant](#variant)|`nvarchar` |Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.|
|[Picture_Comments](#picture_comments)|`nvarchar` ||
|[Product_Price_Id_Text](#product_price_id_text)|`decimal(13, 5)` |Price in the specified currency and for the specified quantity|
|[Product_Id](#product_id)|`uniqueidentifier` |The offered product.|
|[Picture](#picture)|`varbinary` |The actual product picture. Can be NULL if we insert only some comments|
|[Product_Description](#product_description)|`nvarchar` `ML`|The description of the offered product. Initially copied from the name of the offered product.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity offered.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the offered product. It is specified in the measurement unit of Quantity.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Choice_Group_Name](#choice_group_name)|`nvarchar` |Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` `ML`||
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` |Not NULL when the price has been selected from the list of valid standard prices|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Product_Definition_Description](#product_definition_description)|`nvarchar` `ML`|The description of the product|
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Product_Id_Text](#product_id_text)|`nvarchar` `ML`|Name of the item|
|[Offer_Id](#offer_id)|`uniqueidentifier` ||
|[Required_Delivery_Date](#required_delivery_date)|`date` |Date, when the delivery is required. Alternative to Delivery Term Days. When NULL, Delivery Term Days is used.|
|[Offer_Line_Id](#offer_line_id)|`uniqueidentifier` `PK`||

## Columns

### Picture_No

| Property | Value |
| - | - |
|Type|int|

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
|Type|nvarchar|

### Picture_Comments

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Price_Id_Text

| Property | Value |
| - | - |
|Type|decimal(13, 5)|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Choice_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Definition_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Offer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Offer_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


