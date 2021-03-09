# Procedure Inv_Current_Availability_Table_Load


## Summary

| Name | Type | Description |
| - | - | --- |
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serialized items|
|[Enterprise_Company_Id](#enterprise_company_id)|`int` |The enterprise company which issued the document|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which the goods are received or issued.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |Store bin, from/to which the transaction was performed.|
|[Product_Id](#product_id)|`uniqueidentifier` |The item that was received/issued|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Blocked_For_Document_Id](#blocked_for_document_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` ||
|[Product_Cost](#product_cost)|`decimal(0, 0)` ||
|[Store_Cost](#store_cost)|`decimal(0, 0)` ||
|[Base_Cost](#base_cost)|`decimal(0, 0)` ||

## Columns

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|int|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Blocked_For_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


