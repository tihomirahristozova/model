# Query Sys_Default_Values_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` `PK`|Unique id of this default|
|[Column_Name](#column_name)|`nvarchar` |The column for which the default is specified|
|[Table_Name](#table_name)|`nvarchar` |The table, containing the column for which the default value is specified.|
|[Condition_User_Login](#condition_user_login)|`nvarchar` |If not NULL specifies that the default should be applied only if User_Login equals this value|
|[Condition_User_Machine](#condition_user_machine)|`nvarchar` |If not NULL specifies that the default should be applied only if User_Machine equals this value|
|[Condition_Form_Name](#condition_form_name)|`nvarchar` |If not NULL specifies that the default should be applied only if Form_Name equals the specified value|
|[Panel_Name](#panel_name)|`nvarchar` |When not null, specifies the panel for which the default value applies.|

## Columns

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Column_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Table_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_User_Login

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_User_Machine

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Form_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Panel_Name

| Property | Value |
| - | - |
|Type|nvarchar|


