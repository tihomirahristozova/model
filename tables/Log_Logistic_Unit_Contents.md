# Table Log_Logistic_Unit_Contents

Theoretical or actual content of a logistic unit. Entity: Log_Logistic_Unit_Contents (Introduced in version 21.1.0.77)

## Owner Tables Hierarchy

* [Log_Logistic_Units](Log_Logistic_Units.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Content_Id](#logistic_unit_content_id)|`uniqueidentifier` `PK`||
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |The containing logistic unit.|
|[Line_No](#line_no)|`int` |Consecutive position within the logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is contained in the logistic unit.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity of the product in the logistic unit. Expressed in the specified measurement unit.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity.|
|[Standard_Quantity](#standard_quantity)|`decimal(12, 3)` |The quantity, expessed in the standard measurement unit of the product.|
|[Base_Quantity](#base_quantity)|`decimal(12, 3)` |The quantity, expressed in the base measurement category of the product.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Gross_Weight](#gross_weight)|`decimal(12, 3)` |Gross weight in kilograms (kg). NULL means unknown.|
|[Lot_Number](#lot_number)|`nvarchar(32)` |The production lot number. NULL means unknown.|
|[Expiration_Date](#expiration_date)|`date` |Expiration date of the goods. NULL means unknown or N/A.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Logistic_Unit_Content_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

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
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Base_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Gross_Weight

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Expiration_Date

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


