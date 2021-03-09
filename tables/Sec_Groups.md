# Table Sec_Groups

Groups of users. Used for providing group access to secured data. Entity: Sec_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Group_Id](#group_id)|`uniqueidentifier` `PK`||
|[Group_Name](#group_name)|`nvarchar(254)` `ML`||
|[Notes](#notes)|`nvarchar(254)` ||
|[Edit_Period_Days](#edit_period_days)|`int` |The number of days before which the documents can not be corrected, released or voided|
|[Group_Type](#group_type)|`nvarchar(1)` Allowed: `G`, `U`, `A`, `E`, Readonly|Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody|
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
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Edit_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Group_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Group_For_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


