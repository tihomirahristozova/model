# Query Sec_Groups_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Group_Id](#group_id)|`uniqueidentifier` `PK`||
|[Group_Name](#group_name)|`nvarchar` `ML`||
|[Notes](#notes)|`nvarchar` ||
|[Edit_Period_Days](#edit_period_days)|`int` |The number of days before which the documents can not be corrected, released or voided|
|[Group_Type](#group_type)|`nvarchar` Allowed: `G`, `U`, `A`, `E`, Readonly|Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody|
|[Group_For_User_Id](#group_for_user_id)|`uniqueidentifier` Readonly|When Group_Type=U, contains the user for which the group is defined, NULL otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Edit_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Group_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Group_For_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


