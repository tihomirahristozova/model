# Table Ext_Public_User_Lists

Each list represents a unique collection of public users. Entity: Ext_Public_User_Lists

## Summary

| Name | Type | Description |
| - | - | --- |
|[Public_User_List_Id](#public_user_list_id)|`uniqueidentifier` `PK`||
|[Public_User_List_Name](#public_user_list_name)|`nvarchar(64)` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which this list belongs. Null means that the list is available to services offered by all enterprise companies.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Public_User_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Public_User_List_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


