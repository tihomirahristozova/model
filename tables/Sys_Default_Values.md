# Table Sys_Default_Values

Contains user-specified default values for columns in data entry forms. Entity: Sys_Default_Values

## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` `PK`|Unique id of this default|
|[Condition_User_Login](#condition_user_login)|`nvarchar(64)` |If not NULL specifies that the default should be applied only if User_Login equals this value|
|[Condition_User_Machine](#condition_user_machine)|`nvarchar(64)` |If not NULL specifies that the default should be applied only if User_Machine equals this value|
|[Condition_Enterprise_Company_Id](#condition_enterprise_company_id)|`uniqueidentifier` |If not NULL specifies that the default should be applied only if Enterprise_Company_Id equals this value|
|[Condition_Document_Type_Id](#condition_document_type_id)|`uniqueidentifier` |If not NULL specifies that the default should be applied only if Document_Type_Id equals this value|
|[Condition_Form_Name](#condition_form_name)|`nvarchar(64)` |If not NULL specifies that the default should be applied only if Form_Name equals the specified value|
|[Panel_Name](#panel_name)|`nvarchar(64)` |When not null, specifies the panel for which the default value applies.|
|[Table_Name](#table_name)|`nvarchar(64)` |The table, containing the column for which the default value is specified.|
|[Column_Name](#column_name)|`nvarchar(64)` |The column for which the default is specified|
|[Default_Value](#default_value)|`nvarchar(254)` |The default value for Column_Name. Should be applied only if the other conditions are met. NULL specifies NULL default|
|[Condition_Role_Id](#condition_role_id)|`uniqueidentifier` |When not null, specifies that the default value should be applied only when the user plays the specified role.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_User_Login

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Condition_User_Machine

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Condition_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Form_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Panel_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Table_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Column_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Default_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Condition_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


