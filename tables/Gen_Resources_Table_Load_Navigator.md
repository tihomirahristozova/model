# Query Gen_Resources_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Group_Name](#resource_group_name)|`nvarchar` `ML`|Resource group name. Unique within its parent|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which this resource group belongs. NULL means that the group is valid for all companies. Can be NULL only if the parent group company is also NULL|
|[Parent_Resource_Group_Id](#parent_resource_group_id)|`uniqueidentifier` |The parent resource group or NULL if this is root group|
|[Resource_Id](#resource_id)|`uniqueidentifier` `PK`||
|[Resource_Name](#resource_name)|`nvarchar` `ML`|Resource name. Unique within the resource group|
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Costing_Currency_Id](#costing_currency_id)|`uniqueidentifier` |The currency in which resource costs are specified. Required only if resource costs will be specified.|

## Columns

### Resource_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Costing_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


