# Table Scm_Purchase_Product_Prices

Contains purchase prices of the products. Used for automatically loading unit prices in the purchase documents. Entity: Scm_Purchase_Product_Prices

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which a purchase price will be defined|
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |When not null, specifies that the price is valid only for the specified supplier.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |When not null, specifies that this price is valid only when the purchase document is set to work with the specified price list.|
|[Price](#price)|`decimal(13, 5)` |Price in the specified currency and for the specified quantity|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the price|
|[Price_Quantity](#price_quantity)|`decimal(10, 3)` |The quantity of the product for which the price is specified|
|[Price_Quantity_Measurement_Unit_Id](#price_quantity_measurement_unit_id)|`uniqueidentifier` |The measurement unit of Price_Quantity|
|[From_Date](#from_date)|`datetime` |Starting date of validity of the price|
|[Thru_Date](#thru_date)|`datetime` |Ending date (inclusive) of the validity of the price|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the price comparative to other prices|
|[Notes](#notes)|`nvarchar(254)` ||
|[Min_Quantity](#min_quantity)|`decimal(18, 3)` |Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit)|
|[Max_Quantity](#max_quantity)|`decimal(18, 3)` |Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Purchase_Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price

| Property | Value |
| - | - |
|Type|decimal(13, 5)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Quantity

| Property | Value |
| - | - |
|Type|decimal(10, 3)|

### Price_Quantity_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Min_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Max_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


