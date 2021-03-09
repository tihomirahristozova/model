# Table Sec_Domains

Represents one user domain. The users in a domain have different emails. But one user can use the same email to register in different domains. Entity: Sec_Domains (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Domain_Id](#domain_id)|`uniqueidentifier` `PK`||
|[Domain_Name](#domain_name)|`nvarchar(64)` |The name of the domain (restricted for URL usage).|
|[Description](#description)|`nvarchar(256)` `ML`|Multi-language description of the domain.|
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
|Type|nvarchar(64)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(256)|

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


