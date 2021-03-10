# Query Rent_Transaction_Templates_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Rent_Transaction_Template_Id](#rent_transaction_template_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |The route for which the transaction template is defined.|
|[Transaction_Type](#transaction_type)|`nvarchar` Allowed: `D`, `R`, `W`, `S`||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rent_Transaction_Template_Id


Rent_Transaction_Template_Id

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
|Derived From|[Rent_Transaction_Templates](Rent_Transaction_Templates.md).[Rent_Transaction_Template_Id](Rent_Transaction_Templates.md#rent_transaction_template_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Route_Id


Route_Id


The route for which the transaction template is defined.


The route for which the transaction template is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Routes](Wf_Routes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Transaction_Templates](Rent_Transaction_Templates.md).[Route_Id](Rent_Transaction_Templates.md#route_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Transaction_Type


Transaction_Type

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
|Allowed Values|`D`, `R`, `W`, `S`|
|Default Value|None|
|Derived From|[Rent_Transaction_Templates](Rent_Transaction_Templates.md).[Transaction_Type](Rent_Transaction_Templates.md#transaction_type)|
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
|Order|2|
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
|Derived From|[Rent_Transaction_Templates](Rent_Transaction_Templates.md).[Row_Version](Rent_Transaction_Templates.md#row_version)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


