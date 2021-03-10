# Query Sys_Web_Hosts_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Host_Id](#web_host_id)|`uniqueidentifier` `PK`||
|[Web_Host_Name](#web_host_name)|`nvarchar` |The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name.|

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
|Type|nvarchar|
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
|Like|None|no|no|


