# Table Gen_Sequences

Provides numbering sequences, applicable for use in a multi-threaded environment. Entity: Gen_Sequences

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sequence_Id](#sequence_id)|`uniqueidentifier` `PK`||
|[Sequence_Name](#sequence_name)|`nvarchar(50)` ||
|[Simultaneous_Transactions](#simultaneous_transactions)|`bit` |When false, specifies that the users will wait in a queue for a single numbering sequence generator. When true, the system will allow parallel numbering, by using any of the available sequence generators. However, parallel numbering has the drawback that, if no sequence generator is free, it will immediately throw exception, instead of waiting. So before setting to true, make sure that enough sequence generators are available.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sequence_Id


Sequence_Id

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
|Derived From|[Gen_Sequences](Gen_Sequences.md).[Sequence_Id](Gen_Sequences.md#sequence_id)|
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

### Sequence_Name


Sequence_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Sequences](Gen_Sequences.md).[Sequence_Name](Gen_Sequences.md#sequence_name)|
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
|Max Length|50|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Simultaneous_Transactions


Simultaneous_Transactions


When false, specifies that the users will wait in a queue for a single numbering sequence generator. When true, the system will allow parallel numbering, by using any of the available sequence generators. However, parallel numbering has the drawback that, if no sequence generator is free, it will immediately throw exception, instead of waiting. So before setting to true, make sure that enough sequence generators are available.


When false, specifies that the users will wait in a queue for a single numbering sequence generator. When true, the system will allow parallel numbering, by using any of the available sequence generators. However, parallel numbering has the drawback that, if no sequence generator is free, it will immediately throw exception, instead of waiting. So before setting to true, make sure that enough sequence generators are available.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Sequences](Gen_Sequences.md).[Simultaneous_Transactions](Gen_Sequences.md#simultaneous_transactions)|
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
|Derived From|[Gen_Sequences](Gen_Sequences.md).[Row_Version](Gen_Sequences.md#row_version)|
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


