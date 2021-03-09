# Table Sys_Web_Hosts

Contains the names and https certificates of the different host names used to host sites. Entity: Sys_Web_Hosts (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Host_Id](#web_host_id)|`uniqueidentifier` `PK`||
|[Web_Host_Name](#web_host_name)|`nvarchar(2147483647)` |The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name.|
|[Certificate_Type](#certificate_type)|`nvarchar(3)` |The type of certificate uploaded. Currently, only PFX is supported.|
|[Certificate_Original_Filename](#certificate_original_filename)|`nvarchar(254)` |The original name of the file, used to upload the certificate. Used only for reference purposes. When NULL, means that the user did not provide that information when uploading the certificate.|
|[Certificate_Contents](#certificate_contents)|`varbinary` |The contents of the web host certificate. NULL means to use the server system certificate.|
|[Certificate_Password](#certificate_password)|`nvarchar(2147483647)` |The password, which should be used to decrypt the certificate. NULL when the certificate has no password or the system certificate is used.|
|[Certificate_Expiry_Date](#certificate_expiry_date)|`date` |The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When NULL, the expiry date was not provided by the user, when uploading the certificate.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Web_Host_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Host_Name

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Certificate_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Certificate_Original_Filename

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Certificate_Contents

| Property | Value |
| - | - |
|Type|varbinary|

### Certificate_Password

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Certificate_Expiry_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


