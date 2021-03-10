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


Web_Host_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Web_Host_Id](Sys_Web_Hosts.md#web_host_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Web_Host_Name


Web_Host_Name


The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name.


The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Web_Host_Name](Sys_Web_Hosts.md#web_host_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Certificate_Type


Certificate_Type


The type of certificate uploaded. Currently, only PFX is supported.


The type of certificate uploaded. Currently, only PFX is supported.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|PFX|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Certificate_Type](Sys_Web_Hosts.md#certificate_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Certificate_Original_Filename


Certificate_Original_Filename


The original name of the file, used to upload the certificate. Used only for reference purposes. When NULL, means that the user did not provide that information when uploading the certificate.


The original name of the file, used to upload the certificate. Used only for reference purposes. When NULL, means that the user did not provide that information when uploading the certificate.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Certificate_Original_Filename](Sys_Web_Hosts.md#certificate_original_filename)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Certificate_Contents


Certificate_Contents


The contents of the web host certificate. NULL means to use the server system certificate.


The contents of the web host certificate. NULL means to use the server system certificate.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Certificate_Contents](Sys_Web_Hosts.md#certificate_contents)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Certificate_Password


Certificate_Password


The password, which should be used to decrypt the certificate. NULL when the certificate has no password or the system certificate is used.


The password, which should be used to decrypt the certificate. NULL when the certificate has no password or the system certificate is used.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Certificate_Password](Sys_Web_Hosts.md#certificate_password)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|yes|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Certificate_Expiry_Date


Certificate_Expiry_Date


The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When NULL, the expiry date was not provided by the user, when uploading the certificate.


The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When NULL, the expiry date was not provided by the user, when uploading the certificate.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Certificate_Expiry_Date](Sys_Web_Hosts.md#certificate_expiry_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Notes](Sys_Web_Hosts.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Web_Hosts](Sys_Web_Hosts.md).[Row_Version](Sys_Web_Hosts.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


