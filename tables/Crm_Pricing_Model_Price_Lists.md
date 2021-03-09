# Table Crm_Pricing_Model_Price_Lists

The price lists, which are updated by the pricing model. Entity: Crm_Pricing_Model_Price_Lists

## Owner Tables Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pricing_Model_Price_List_Id](#pricing_model_price_list_id)|`uniqueidentifier` `PK`|Pricing Model Price List|
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` |The pricing model, for which the price list is listed|
|[Line_No](#line_no)|`int` |The consecutive number of this price list within the pricing model|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |The price list, which is included in the pricing model|
|[Margin_Percent](#margin_percent)|`decimal(6, 5)` |Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. NULL, when the price will not be automatically calculated in this way|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pricing_Model_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pricing_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Margin_Percent

| Property | Value |
| - | - |
|Type|decimal(6, 5)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


