# Table Sec_Trusted_Application_Authorizations

Authorization of a trusted application to access the data on behalf of a context user. Entity: Sec_Trusted_Application_Authorizations (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Sec_Trusted_Applications](Sec_Trusted_Applications.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Trusted_Application_Authorization_Id](#trusted_application_authorization_id)|`uniqueidentifier` `PK`||
|[Trusted_Application_Id](#trusted_application_id)|`uniqueidentifier` |The application, which is authorized.|
|[Granting_User_Id](#granting_user_id)|`uniqueidentifier` |The user, who authorized the application.|
|[Context_User_Id](#context_user_id)|`uniqueidentifier` |The user, whose permissions are granted to the application.|
|[Grant_Time_Utc](#grant_time_utc)|`datetime` |The time (in UTC) when the authorization was granted.|
|[Valid_From_Utc](#valid_from_utc)|`datetime` |The start of the validitiy of the authorization. NULL means that there is no restriction.|
|[Valid_Until_Utc](#valid_until_utc)|`datetime` |The time (in UTC) when the grant expires. NULL means that there is no time restriction.|
|[Is_Revoked](#is_revoked)|`bit` |Specifies whether the grant is explicitly revoked.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Trusted_Application_Authorization_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Trusted_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Granting_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Context_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Grant_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Valid_From_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Valid_Until_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Is_Revoked

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


