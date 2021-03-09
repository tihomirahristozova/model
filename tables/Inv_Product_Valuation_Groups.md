# Table Inv_Product_Valuation_Groups

Contains the available valuation groups for products. They are used in reconciliations, where all pluses and minuses within a valuation group are allowed to balance each other without fiscal effects. Without valuation groups, each product is balanced for itself and taxes are calculated for each surplus. Entity: Inv_Product_Valuation_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Valuation_Group_Id](#valuation_group_id)|`uniqueidentifier` `PK`||
|[Valuation_Group_Code](#valuation_group_code)|`nvarchar(64)` |The unique code of the product valuation group.|
|[Valuation_Group_Name](#valuation_group_name)|`nvarchar(128)` `ML`|The name of the product valuation group.|
|[Description](#description)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Valuation_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Valuation_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


