# Table Rent_Assets

Contains the rentable assets. Entity: Rent_Assets

## Owner Tables Hierarchy

* [Rent_Asset_Groups](Rent_Asset_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rental_Asset_Id](#rental_asset_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Type_Id](#rental_asset_type_id)|`uniqueidentifier` |The type of the asset.|
|[Rental_Asset_Group_Id](#rental_asset_group_id)|`uniqueidentifier` |The logical group of the rental asset.|
|[Rental_Asset_Code](#rental_asset_code)|`nvarchar(20)` |Unique rental asset code|
|[Rental_Asset_Name](#rental_asset_name)|`nvarchar(254)` |The name of the rental asset.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Accounting_Asset_Id](#accounting_asset_id)|`uniqueidentifier` |When not NULL identifies the corresponding accounting asset|
|[Sales_Product_Id](#sales_product_id)|`uniqueidentifier` ||
|[Work_Schedule_Id](#work_schedule_id)|`uniqueidentifier` ||
|[Time_Period_Type](#time_period_type)|`nvarchar(1)` Allowed: `D`, `M`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Standard_Guarantee_Amount](#standard_guarantee_amount)|`decimal(14, 2)` ||
|[Standard_Guarantee_Amount_Currency_Id](#standard_guarantee_amount_currency_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||

## Columns

### Rental_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Rental_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Accounting_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time_Period_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Guarantee_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Standard_Guarantee_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


