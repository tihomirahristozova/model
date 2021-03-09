# Query Sys_Web_Sites_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` `PK`||
|[Web_Site_Type](#web_site_type)|`nvarchar` Allowed: `API`, `CC`, `ID`, `EC`, `LEG`, `SI`, `DM`, `PFL`, `APP`, `TAP`, `DAP`, `WMS`|The type of web site - Api, Client Center, Id, etc.|
|[Relative_Url](#relative_url)|`nvarchar` |The relative Url of the site. This is the text after the first slash after the protocol and host name. The text should not include the protocol and host name. NULL means that the site will be hosted as the root site in the speicified web host.|

## Columns

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Site_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Relative_Url

| Property | Value |
| - | - |
|Type|nvarchar|


