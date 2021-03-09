# Table Crm_Product_Distribution_Channels

Channel assignments (listing) for products. Entity: Crm_Product_Distribution_Channels

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Id](#product_id)|`uniqueidentifier` |The listed product|
|[Product_Distribution_Channel_Id](#product_distribution_channel_id)|`uniqueidentifier` `PK`|Product, listed at distribution channel|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |The distribution channel in which the product is listed|
|[From_Date](#from_date)|`date` |When the product was listed. NULL-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)|
|[To_Date](#to_date)|`date` |When the product was de-listed. NULL=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)|
|[Is_Active](#is_active)|`bit` |Is this product listing active? 1=Yes, 0=No|
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(18, 4)` |Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(18, 3)` |Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribution_Channel_Id

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

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Minimal_Sales_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Minimal_Sales_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


