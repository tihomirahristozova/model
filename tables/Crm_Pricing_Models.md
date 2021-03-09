# Table Crm_Pricing_Models

Pricing models are assigned to product groups and are used to automate creation of standard costs and prices and related price records. Entity: Crm_Pricing_Models

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` `PK`|Pricing Model|
|[Pricing_Model_Name](#pricing_model_name)|`nvarchar(254)` |The name of the pricing model|
|[Default_Margin_Percent](#default_margin_percent)|`decimal(6, 5)` |Default margin between standard cost and standard price. The margin is applied to the products when calculating standard price|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency in which the prices will be calculated|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |Purchase price list Id, which will be used to get the purchase price of the products|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pricing_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pricing_Model_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Margin_Percent

| Property | Value |
| - | - |
|Type|decimal(6, 5)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


