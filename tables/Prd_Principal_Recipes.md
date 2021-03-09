# Table Prd_Principal_Recipes

List of base recipe models. Recipe models are used by the Product Configurator to create specific recipes. Entity: Prd_Principal_Recipes

## Owner Tables Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|The principal recipe unique id|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |The production group, whose production is defined by the principal recipe |
|[Principal_Recipe_Name](#principal_recipe_name)|`nvarchar(64)` |Name of the principal recipe|
|[Release_Date](#release_date)|`datetime` |The date, when the recipe model is released for use|
|[Expiry_Date](#expiry_date)|`datetime` |The last date, when the recipe should be used. NULL means that there is no expiry date yet and the recipe model is still active.|
|[Duration_Hour](#duration_hour)|`decimal(10, 0)` |The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time.|
|[Produce_Quantity](#produce_quantity)|`decimal(18, 3)` |Suggested quantity to produce. Usually it is equal to 1|
|[Produce_Unit_Id](#produce_unit_id)|`uniqueidentifier` |The measurement unit of Produce_Quantity. The selected item must support the specified unit|
|[Routing_Id](#routing_id)|`uniqueidentifier` |The routing to be used for the recipes. NULL means that the workorders will not use routing|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe.|
|[Notes](#notes)|`nvarchar(254)` |User comments for the principal recipe.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### Duration_Hour

| Property | Value |
| - | - |
|Type|decimal(10, 0)|

### Produce_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Produce_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Routing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


