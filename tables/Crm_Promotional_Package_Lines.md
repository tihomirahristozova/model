# Table Crm_Promotional_Package_Lines

Detail records (lines) of promotional package definition. Entity: Crm_Promotional_Package_Lines

## Owner Tables Hierarchy

* [Crm_Promotional_Packages](Crm_Promotional_Packages.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Promotional_Package_Line_Id](#promotional_package_line_id)|`uniqueidentifier` `PK`||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` ||
|[Line_Number](#line_number)|`int` |Consecutive line number|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is included in the promotional package|
|[Quantity](#quantity)|`decimal(9, 3)` |The quantity of the product in the package in the base measurement unit of the Product.|
|[Standard_Discount_Percent_Adjust](#standard_discount_percent_adjust)|`decimal(7, 6)` |The value of change (in percents) for the standard discount|
|[Standard_Discount_Adjust_Or_Replace](#standard_discount_adjust_or_replace)|`nvarchar(1)` Allowed: `A`, `R`, `M`|Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount|
|[Unit_Price](#unit_price)|`decimal(13, 5)` |When not null specifies directly unit price for the product. When NULL, the package specifies only discount|
|[Unit_Price_Currency_Id](#unit_price_currency_id)|`uniqueidentifier` |Currency of the unit price. NULL if the package specifies only discount|
|[Row_Version](#row_version)|`timestamp` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Product lot number in the promotional package.|

## Columns

### Promotional_Package_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Number

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Standard_Discount_Percent_Adjust

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Standard_Discount_Adjust_Or_Replace

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(13, 5)|

### Unit_Price_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


