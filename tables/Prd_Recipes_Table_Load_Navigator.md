# Query Prd_Recipes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Recipe_Name](#recipe_name)|`nvarchar` ||
|[Release_Date](#release_date)|`datetime` ||
|[Expiry_Date](#expiry_date)|`datetime` ||
|[Produce_Quantity](#produce_quantity)|`decimal(0, 0)` ||
|[Routing_Id](#routing_id)|`uniqueidentifier` |The routing used to create the product. NULL means that workorders might not use routing.|
|[Scrap_Rate](#scrap_rate)|`decimal(0, 0)` ||
|[Price](#price)|`decimal(0, 0)` ||
|[Price_Per_Lot](#price_per_lot)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` ||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |Currency directory, which is used to convert the costs and prices of materials, operations and resources into the currency of the product.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store for which this technology is valid. The store is matched with the output store specified in the production order. When NULL, the technology is valid for all stores.|
|[Row_Version](#row_version)|`timestamp` ||
|[Description](#description)|`nvarchar` `ML`||
|[Produce_Quantity_AMU](#produce_quantity_amu)|`decimal(0, 0)` ||
|[Additional_Measurement_Unit_Id](#additional_measurement_unit_id)|`uniqueidentifier` ||
|[Materials_Cost](#materials_cost)|`decimal(0, 0)` ||
|[Operations_Cost](#operations_cost)|`decimal(0, 0)` ||
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` Readonly||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Produce_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Routing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Price

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Produce_Quantity_AMU

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Additional_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Materials_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Operations_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


