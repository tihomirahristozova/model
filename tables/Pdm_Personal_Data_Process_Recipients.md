# Table Pdm_Personal_Data_Process_Recipients

Contains recipients, to which personal data is disclosed. Entity: Pdm_Personal_Data_Process_Recipients (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Personal_Data_Process_Recipient_Id](#personal_data_process_recipient_id)|`uniqueidentifier` `PK`||
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The process, whose data is disclosed to the recipient.|
|[Recipient_Party_Id](#recipient_party_id)|`uniqueidentifier` |The recipient, to whom the data is disclosed.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Personal_Data_Process_Recipient_Id


Personal_Data_Process_Recipient_Id

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
|Derived From|[Pdm_Personal_Data_Process_Recipients](Pdm_Personal_Data_Process_Recipients.md).[Personal_Data_Process_Recipient_Id](Pdm_Personal_Data_Process_Recipients.md#personal_data_process_recipient_id)|
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

### Personal_Data_Process_Id


Personal_Data_Process_Id


The process, whose data is disclosed to the recipient.


The process, whose data is disclosed to the recipient.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Process_Recipients](Pdm_Personal_Data_Process_Recipients.md).[Personal_Data_Process_Id](Pdm_Personal_Data_Process_Recipients.md#personal_data_process_id)|
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

### Recipient_Party_Id


Recipient_Party_Id


The recipient, to whom the data is disclosed.


The recipient, to whom the data is disclosed.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Process_Recipients](Pdm_Personal_Data_Process_Recipients.md).[Recipient_Party_Id](Pdm_Personal_Data_Process_Recipients.md#recipient_party_id)|
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
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Process_Recipients](Pdm_Personal_Data_Process_Recipients.md).[Notes](Pdm_Personal_Data_Process_Recipients.md#notes)|
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
|Derived From|[Pdm_Personal_Data_Process_Recipients](Pdm_Personal_Data_Process_Recipients.md).[Row_Version](Pdm_Personal_Data_Process_Recipients.md#row_version)|
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


