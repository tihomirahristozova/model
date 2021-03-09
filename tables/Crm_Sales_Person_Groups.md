# Table Crm_Sales_Person_Groups

Hierarchical sales person grouping. Entity: Crm_Sales_Person_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Group_Name](#sales_person_group_name)|`nvarchar(128)` ||
|[Sales_Person_Group_Code](#sales_person_group_code)|`nvarchar(64)` ||
|[Parent_Sales_Person_Group_Id](#parent_sales_person_group_id)|`uniqueidentifier` |The parent sales person group in the hierarchy.|
|[Full_Path](#full_path)|`nvarchar(4000)` Readonly|Full path to this item in the form /root/child1/../leaf/|
|[Manager_Person_Id](#manager_person_id)|`uniqueidentifier` |The manager of the group. NULL when there is no manager.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Sales_Person_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Parent_Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(4000)|

### Manager_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


