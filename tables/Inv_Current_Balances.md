# View Inv_Current_Balances

The current inventory balances, grouped by storage key (Store, Product, Lot, etc.). Entity: Inv_Current_Balances

## Summary

| Name | Type | Description |
| - | - | --- |
|[Quantity_Base](#quantity_base)|`decimal(38, 3)` Readonly|The quantity of the stock received/issued in base measurement unit|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |Store bin, from/to which the transaction was performed.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serialized items|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Product_Cost](#product_cost)|`decimal(38, 2)` |The cost of the inventory in the products currency.|
|[Store_Cost](#store_cost)|`decimal(38, 2)` |The cost of the inventory in the stores currency.|
|[Base_Cost](#base_cost)|`decimal(38, 2)` |The cost of the inventory in base currency of the enterprise company.|

## Columns

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Cost

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Store_Cost

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Base_Cost

| Property | Value |
| - | - |
|Type|decimal(38, 2)|


