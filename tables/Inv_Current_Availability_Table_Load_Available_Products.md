# Procedure Inv_Current_Availability_Table_Load_Available_Products


## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` `PK`||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` |Standard sales price (used if no special price is defined) for one standard lot of the product in the currency, specified by Costing_Currency_Id|
|[Is_Featured](#is_featured)|`bit` ||
|[Expiry_Date](#expiry_date)|`datetime` Readonly||

## Columns

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Is_Featured

| Property | Value |
| - | - |
|Type|bit|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|


