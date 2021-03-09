# Table Sys_Web_Sites

Contains the web sites, which are hosted for the database. Entity: Sys_Web_Sites (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company, for which is the site. NULL means, that the web site should not be enterprise company specific.|
|[Web_Site_Type](#web_site_type)|`nvarchar(3)` Allowed: `API`, `CC`, `ID`, `EC`, `LEG`, `SI`, `DM`, `PFL`, `APP`, `TAP`, `DAP`, `WMS`|The type of web site - Api, Client Center, Id, etc.|
|[Web_Host_Id](#web_host_id)|`uniqueidentifier` |The web host in which to host the site.|
|[Relative_Url](#relative_url)|`nvarchar(254)` |The relative Url of the site. This is the text after the first slash after the protocol and host name. The text should not include the protocol and host name. NULL means that the site will be hosted as the root site in the speicified web host.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |Indicates whether the web site is active and will be instantiated upon next web server restart.|
|[Row_Version](#row_version)|`timestamp` ||
|[Trusted_Application_Id](#trusted_application_id)|`uniqueidentifier` |The trusted application related to this web site|

## Columns

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Site_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Web_Host_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Relative_Url

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Trusted_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


