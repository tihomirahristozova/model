# Table Prj_Type_Work_Types

Contains the work types, that can be performed in projects of this project type. Entity: Prj_Type_Work_Types

## Owner Tables Hierarchy

* [Prj_Types](Prj_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` `PK`||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` ||
|[Work_Type_Name](#work_type_name)|`nvarchar(254)` |The name of the work type.|
|[Billed_With_Product_Id](#billed_with_product_id)|`uniqueidentifier` |The product, which is used for billing purposes for this work type. The price of the product is also used for project budgeting. NULL means that the work type cannot be billed|
|[Is_Active](#is_active)|`bit` |True when the work type is currently active and selectable in new documents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Work_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Billed_With_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


