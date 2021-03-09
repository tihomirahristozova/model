# Table Crm_Forecast_Items

Forecast items form demand in MRP calculations. Entity: Crm_Forecast_Items

## Summary

| Name | Type | Description |
| - | - | --- |
|[Forecast_Item_Id](#forecast_item_id)|`uniqueidentifier` `PK`||
|[Country_Id](#country_id)|`uniqueidentifier` |The country for which the forecast is made. When NULL, the forecast is country neutral.|
|[Dealer_Id](#dealer_id)|`uniqueidentifier` |The dealer for which the forecast is made. When NULL, the forecast is not for any specfic dealer.|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |The sales person for which the forecast is made. When NULL, the forecast is not for any specfic sales person.|
|[Customer_Id](#customer_id)|`uniqueidentifier` |The customer for which the forecast is made. When NULL, the forecast is not for any specfic customer.|
|[Date](#date)|`datetime` |The date for which the sales is forecasted. When forecasting for a period, this contains the first date of the period|
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which the forecast is made.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store which is expected to sell the products.|
|[Quantity](#quantity)|`decimal(18, 3)` |The forecasted sales quantity in the base measurement category of the product|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Forecast_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Date

| Property | Value |
| - | - |
|Type|datetime|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


