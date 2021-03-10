# Table Gen_Document_Jobs

Represents jobs, which change state of documents. Entity: Gen_Document_Jobs (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Sys_Jobs](Sys_Jobs.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Job_Id](#document_job_id)|`uniqueidentifier` `PK`||
|[Job_Id](#job_id)|`uniqueidentifier` |The id of the general job.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The type of the document, whose state will be changed.|
|[Filter_Xml](#filter_xml)|`nvarchar(2147483647)` |Specifies the documents, whose state will be changed.|
|[New_State](#new_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`|Specifies the state, which should be set to the documents, matching the filter.|
|[Row_Version](#row_version)|`timestamp` ||
|[New_User_Status_Id](#new_user_status_id)|`uniqueidentifier` |Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type.|

## Columns

### Document_Job_Id


Document_Job_Id

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
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[Document_Job_Id](Gen_Document_Jobs.md#document_job_id)|
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

### Job_Id


Job_Id


The id of the general job.


The id of the general job.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Jobs](Sys_Jobs.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[Job_Id](Gen_Document_Jobs.md#job_id)|
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

### Document_Type_Id


Document_Type_Id


The type of the document, whose state will be changed.


The type of the document, whose state will be changed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[Document_Type_Id](Gen_Document_Jobs.md#document_type_id)|
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

### Filter_Xml


Filter_Xml


Specifies the documents, whose state will be changed.


Specifies the documents, whose state will be changed.

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
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[Filter_Xml](Gen_Document_Jobs.md#filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
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

### New_State


New_State


Specifies the state, which should be set to the documents, matching the filter.


Specifies the state, which should be set to the documents, matching the filter.

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `10`, `20`, `30`, `40`, `50`, `5`|
|Default Value|None|
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[New_State](Gen_Document_Jobs.md#new_state)|
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
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[Row_Version](Gen_Document_Jobs.md#row_version)|
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

### New_User_Status_Id


New_User_Status_Id


Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type.


Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Type_User_Statuses](Gen_Document_Type_User_Statuses.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Jobs](Gen_Document_Jobs.md).[New_User_Status_Id](Gen_Document_Jobs.md#new_user_status_id)|
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


