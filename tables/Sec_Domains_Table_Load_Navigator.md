# Query Sec_Domains_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Domain_Id](#domain_id)|`uniqueidentifier` `PK`||
|[Domain_Name](#domain_name)|`nvarchar` |The name of the domain (restricted for URL usage).|
|[Description](#description)|`nvarchar` `ML`|Multi-language description of the domain.|
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Default](#is_default)|`bit` |Specifies whether this is the default domain for the database.|
|[Allow_Local_Accounts](#allow_local_accounts)|`bit` |Specifies whether users can have local accounts with locally stored passwords in the DB (not recommended).|

## Columns

### Domain_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Domain_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Allow_Local_Accounts

| Property | Value |
| - | - |
|Type|bit|


