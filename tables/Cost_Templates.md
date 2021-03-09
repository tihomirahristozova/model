# Table Cost_Templates

Cost templates specify how to calculate and allocate costs. Entity: Cost_Templates

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Template_Id](#cost_template_id)|`uniqueidentifier` `PK`||
|[Cost_Template_Code](#cost_template_code)|`nvarchar(16)` |Unique code of the cost template.|
|[Cost_Template_Name](#cost_template_name)|`nvarchar(254)` |Name of the cost template.|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the calculations, based on the template|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Template_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Cost_Template_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


