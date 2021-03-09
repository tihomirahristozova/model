# Table Prd_Work_Order_Item_Ingredients

The materials consumed in the production order operations. Entity: Prd_Work_Order_Item_Ingredients

## Owner Tables Hierarchy

* [Prd_Work_Orders](Prd_Work_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The order of the line within the item.|
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` |The work order item for which the materials in this line are used. If NULL means that the materials are distributed amongst all work order items in the document.|
|[Material_Id](#material_id)|`uniqueidentifier` |The Id of the consumed material (Gen_Products_Table)|
|[Used_Quantity](#used_quantity)|`decimal(18, 3)` |The quantity of the material consumed in the operation|
|[Used_Quantity_Unit_Id](#used_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity of the material consumed in the operation|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to retrieve the material.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Id](#id)|`uniqueidentifier` `PK`|The Id of the production order operation|
|[Row_Version](#row_version)|`timestamp` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies the serial number of the ingredient|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |Lot from which to get the material. When NULL, any lot can be used.|
|[Used_Quantity_Base](#used_quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Used Quantity in the base measurement category of the material.|
|[Operation_Id](#operation_id)|`uniqueidentifier` |Specifies for which operation this ingredient is used|
|[Distribute_By](#distribute_by)|`nvarchar(2)` Allowed: `SP`, `MC`, `SC`|Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT NULL iif Work_Order_Item_Id is NULL. MC=Measurement, SP=Standard_Price|
|[Principal_Recipe_Ingredient_Id](#principal_recipe_ingredient_id)|`uniqueidentifier` |The principal recipe ingredient on which this record is based.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin from which to take the ingredients|
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(18, 3)` |The quantity of the material, which will be used for setup.|
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` ||
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` |Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT NULL iif Distribute_By = MC.|
|[Used_Standard_Quantity_Base](#used_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. NULL means to take the value from Used Quantity Base.|

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

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

### Used_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribute_By

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Principal_Recipe_Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fixed_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribute_By_Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Used_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


