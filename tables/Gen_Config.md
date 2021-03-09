# Table Gen_Config

Hierarchical repository of configuration options. Entity: Gen_Config

## Summary

| Name | Type | Description |
| - | - | --- |
|[Config_Id](#config_id)|`uniqueidentifier` `PK`||
|[Key_Path](#key_path)|`nvarchar(128)` |Full path of the configuration option|
|[Description](#description)|`nvarchar(254)` ||
|[User_Login](#user_login)|`nvarchar(64)` |If not NULL, the configuration option is specific to the user|
|[User_Machine](#user_machine)|`nvarchar(64)` |If not NULL, the configuration option is specific to the machine|
|[Key_Value](#key_value)|`nvarchar(1073741823)` |The value of the configuration option|
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Indicates whether this config entry is active. Inactive config entries are not taken into account.|

## Columns

### Config_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Key_Path

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### User_Login

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### User_Machine

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Key_Value

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


