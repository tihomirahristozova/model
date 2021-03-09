# Table Gen_Resource_Groups

Resource groups categorize the resources. Entity: Gen_Resource_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` `PK`|Resource Group Id|
|[Resource_Group_Name](#resource_group_name)|`nvarchar(254)` `ML`|Resource group name. Unique within its parent|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which this resource group belongs. NULL means that the group is valid for all companies. Can be NULL only if the parent group company is also NULL|
|[Parent_Resource_Group_Id](#parent_resource_group_id)|`uniqueidentifier` |The parent resource group or NULL if this is root group|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


