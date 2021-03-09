# Procedure Crm_Sales_Orders_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the sales order|
|[Product_Id](#product_id)|`uniqueidentifier` |The product sold|
|[Product_Description](#product_description)|`nvarchar` `ML`|The name of the sold product at the time the sale was made|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity sold|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |Unit price of the product in the currency of the sales order and in the unit of measure, as specified by QuantityUnitId|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total amount for the line. Equals to Quantity * Unit_Price, less the discounts|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |User-defined discount for the line|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |The line discount type used to form the Line_Standard_Discount_Percent|
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` Readonly|Standard discount for the line. This is automatically computed according to discount conditions|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` |Not NULL when the price has been selected from the list of valid standard prices|
|[Required_Delivery_Date](#required_delivery_date)|`date` |The required (contracted) delivery date for the line|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` `PK`||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type to be passed to the invoice line. If deal type in entered then the invoice creates VAT entry for this deal type.|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` `ML`|Name of the measurement unit|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` Readonly||
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Product_Id_Text](#product_id_text)|`nvarchar` `ML`|Name of the item|
|[Line_Discount_Id_Text](#line_discount_id_text)|`nvarchar` ||
|[Product_Price_Id_Text](#product_price_id_text)|`decimal(0, 0)` ||
|[Return_For_Sales_Order_Line_Id](#return_for_sales_order_line_id)|`uniqueidentifier` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Line_Discount_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Price_Id_Text

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Return_For_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


