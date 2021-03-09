# Procedure Prd_Work_Orders_Table_Load_Environment_Item_Ingredients


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|The Id of the production order operation|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The Id of the work order, containing the item|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item for which the materials in this line are used. If NULL means that the materials are distributed amongst all work order items in the document.|
|[Material_Id](#material_id)|`uniqueidentifier` ||
|[Used_Quantity](#used_quantity)|`decimal(18, 3)` |The quantity of the material consumed in the operation|
|[Line_Ord](#line_ord)|`int` |The order of the line within the item.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to retrieve the material.|
|[Notes](#notes)|`nvarchar` ||
|[Used_Quantity_Unit_Id](#used_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity of the material consumed in the operation|
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(18, 3)` |The quantity of the material, which will be used for setup.|
|[Operation_Id](#operation_id)|`uniqueidentifier` ||
|[Principal_Recipe_Ingredient_Id](#principal_recipe_ingredient_id)|`uniqueidentifier` ||
|[Distribute_By](#distribute_by)|`nvarchar` ||
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` ||
|[Used_Quantity_Base](#used_quantity_base)|`decimal(0, 0)` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Used_Standard_Quantity_Base](#used_standard_quantity_base)|`decimal(0, 0)` ||
|[Standard_Price_Per_Lot](#standard_price_per_lot)|`decimal(0, 0)` ||
|[Standard_Cost_Per_Lot](#standard_cost_per_lot)|`decimal(0, 0)` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Used_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fixed_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribute_By

| Property | Value |
| - | - |
|Type|nvarchar|

### Distribute_By_Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Standard_Cost_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


