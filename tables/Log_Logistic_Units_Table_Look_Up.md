# Query Log_Logistic_Units_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` `PK`||
|[Serial_Code](#serial_code)|`nvarchar` |Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC.|

## Columns

### Logistic_Unit_Id


Logistic_Unit_Id

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
|Derived From|[Log_Logistic_Units](Log_Logistic_Units.md).[Logistic_Unit_Id](Log_Logistic_Units.md#logistic_unit_id)|
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

### Serial_Code


Serial_Code


Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC.


Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC.

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
|Derived From|[Log_Logistic_Units](Log_Logistic_Units.md).[Serial_Code](Log_Logistic_Units.md#serial_code)|
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


