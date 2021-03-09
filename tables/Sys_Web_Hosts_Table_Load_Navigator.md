# Query Sys_Web_Hosts_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Row_Version](#row_version)|`timestamp` ||
|[Web_Host_Id](#web_host_id)|`uniqueidentifier` `PK`||
|[Web_Host_Name](#web_host_name)|`nvarchar` |The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name.|
|[Certificate_Type](#certificate_type)|`nvarchar` |The type of certificate uploaded. Currently, only PFX is supported.|
|[Certificate_Original_Filename](#certificate_original_filename)|`nvarchar` |The original name of the file, used to upload the certificate. Used only for reference purposes. When NULL, means that the user did not provide that information when uploading the certificate.|
|[Certificate_Expiry_Date](#certificate_expiry_date)|`date` |The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When NULL, the expiry date was not provided by the user, when uploading the certificate.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Web_Host_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Host_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Certificate_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Certificate_Original_Filename

| Property | Value |
| - | - |
|Type|nvarchar|

### Certificate_Expiry_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


