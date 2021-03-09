# Table Crm_Product_Prices

Specific prices of products. A price is applied after matching the specified criteria. Entity: Crm_Product_Prices

## Summary

| Name | Type | Description |
| - | - | --- |
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |When not NULL, specifies that the sales document must have the specified price list.|
|[Price](#price)|`decimal(13, 5)` |Price in the specified currency and for the specified quantity|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the price|
|[Price_Quantity_Measurement_Unit_Id](#price_quantity_measurement_unit_id)|`uniqueidentifier` |The measurement unit of Price_Quantity|
|[Customer_Id](#customer_id)|`uniqueidentifier` |When not NULL, specifies that the customer of the sales document must be the specified customer.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the sales document must be in the specified enterprise company.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the price comparative to other prices. Only the highest priority price is applied.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Min_Quantity](#min_quantity)|`decimal(18, 3)` |Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit)|
|[Max_Quantity](#max_quantity)|`decimal(18, 3)` |Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit|
|[From_Date](#from_date)|`date` |Starting date of validity of the price|
|[Thru_Date](#thru_date)|`date` |Ending date (inclusive) of the validity of the price|
|[Target_Group_Id](#target_group_id)|`uniqueidentifier` |When not NULL, specifies a criteria, which is matched only when the customer of the sales document is included in the group.|
|[Price_Type_Id](#price_type_id)|`uniqueidentifier` |Price type of the current product price. The price types are used to set additional priority condition for the prices.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company location.|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |Use the price only when selling through the specified channel|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` `PK`||
|[Price_Quantity](#price_quantity)|`decimal(10, 3)` |The quantity of the product for which the price is specified|
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which a price will be defined|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Price_List_Id

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

### Price_Quantity_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### From_Date

| Property | Value |
| - | - |
|Type|date|

### Thru_Date

| Property | Value |
| - | - |
|Type|date|

### Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_Quantity

| Property | Value |
| - | - |
|Type|decimal(10, 3)|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


