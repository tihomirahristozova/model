# Table Acc_Account_Groups

Hierarchical chart of account groups. Entity: Acc_Account_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Account_Group_Id](#account_group_id)|`uniqueidentifier` `PK`||
|[Parent_Account_Group_Id](#parent_account_group_id)|`uniqueidentifier` |Parent account group. NULL if this is root group|
|[Account_Group_Number](#account_group_number)|`nvarchar(30)` |Unique account group number. May contain characters, if required|
|[Account_Group_Name](#account_group_name)|`nvarchar(160)` `ML`|Account group name, required. Must be unique within the parent group|
|[Full_Path](#full_path)|`nvarchar(256)` |Full path to the group. Contains delimited list of group numbers of parent groups|
|[Description](#description)|`nvarchar(254)` `ML`||
|[Discontinued](#discontinued)|`bit` |1 means that the account group won't be used any more and should not appear in combo boxes|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Group_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|

### Account_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(160)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Discontinued

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


