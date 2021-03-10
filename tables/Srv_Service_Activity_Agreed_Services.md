# Table Srv_Service_Activity_Agreed_Services

Contains the services, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Services

## Owner Tables Hierarchy

* [Srv_Service_Activity_Services](Srv_Service_Activity_Services.md)
* [Srv_Service_Activities](Srv_Service_Activities.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Service_Activity_Service_Id](#service_activity_service_id)|`uniqueidentifier` Readonly||
|[Service_Agreement_Service_Id](#service_agreement_service_id)|`uniqueidentifier` Readonly|Service agreement service line that records the paid or agreed in advance service or product|
|[Agreed_Quantity](#agreed_quantity)|`decimal(18, 3)` Readonly|Quantity from the service agreement service line that is accounted for this service activity service line|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id

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
|Derived From|[Srv_Service_Activity_Agreed_Services](Srv_Service_Activity_Agreed_Services.md).[Id](Srv_Service_Activity_Agreed_Services.md#id)|
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
|Equals|NULL|no|yes|

### Service_Activity_Service_Id


Service_Activity_Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Srv_Service_Activity_Services](Srv_Service_Activity_Services.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Srv_Service_Activity_Agreed_Services](Srv_Service_Activity_Agreed_Services.md).[Service_Activity_Service_Id](Srv_Service_Activity_Agreed_Services.md#service_activity_service_id)|
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

### Service_Agreement_Service_Id


Service_Agreement_Service_Id


Service agreement service line that records the paid or agreed in advance service or product


Service agreement service line that records the paid or agreed in advance service or product

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Srv_Service_Agreement_Services](Srv_Service_Agreement_Services.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Srv_Service_Activity_Agreed_Services](Srv_Service_Activity_Agreed_Services.md).[Service_Agreement_Service_Id](Srv_Service_Activity_Agreed_Services.md#service_agreement_service_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Agreed_Quantity


Agreed_Quantity


Quantity from the service agreement service line that is accounted for this service activity service line


Quantity from the service agreement service line that is accounted for this service activity service line

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Srv_Service_Activity_Agreed_Services](Srv_Service_Activity_Agreed_Services.md).[Agreed_Quantity](Srv_Service_Activity_Agreed_Services.md#agreed_quantity)|
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
|Derived From|[Srv_Service_Activity_Agreed_Services](Srv_Service_Activity_Agreed_Services.md).[Row_Version](Srv_Service_Activity_Agreed_Services.md#row_version)|
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


