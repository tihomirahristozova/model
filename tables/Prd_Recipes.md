# Table Prd_Recipes

Contains the characteristics of operations used to create products. Entity: Prd_Recipes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Recipe_Name](#recipe_name)|`nvarchar(64)` |The name of the recipe. When there is only 1 recipe, it is often equal to the product name. However, when there are multiple recipes for one product, the name is used for diferentiation.|
|[Id](#id)|`uniqueidentifier` `PK`|Unique recipe Id|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |Currency directory, which is used to convert the costs and prices of materials, operations and resources into the currency of the product.|
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Is_Default](#is_default)|`bit` |Default for period: Release_Date - Expiry_Date|
|[Notes](#notes)|`nvarchar(254)` |User comments for the recipe|
|[Price_Per_Lot](#price_per_lot)|`decimal(18, 4)` |Price for one lot of the product (according to Lot_Size_Quantity_Base)|
|[Price](#price)|`decimal(18, 4)` |The price for the specified Produce_Quantity|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |The percentage (0..1) of scrap usually occurring during the operation. Specifying this leads to inflated requirements of all raw materials for this recipe|
|[Routing_Id](#routing_id)|`uniqueidentifier` |The routing used to create the product. NULL means that workorders might not use routing.|
|[Produce_Quantity](#produce_quantity)|`decimal(18, 3)` |Lot size. This is the produced quantity in one production run. The quantity is measured in the primary unit of Product_Id|
|[Expiry_Date](#expiry_date)|`datetime` |The last date, when the recipe should be used. NULL means that the recipe might still be in use|
|[Release_Date](#release_date)|`datetime` |The date, when the recipe was released to production|
|[Product_Id](#product_id)|`uniqueidentifier` |The Id of the produced product|
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` |The prinicipal recipe, used to create this recipe. NULL means that this recipe was created without the help of principal recipe|
|[Store_Id](#store_id)|`uniqueidentifier` |The store for which this technology is valid. The store is matched with the output store specified in the production order. When NULL, the technology is valid for all stores.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Recipe_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Price_Per_Lot

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Price

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Routing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Produce_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Id

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


