# Query Its_Declarations_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Reference_Year](#reference_year)|`smallint` |Year, for which the declaration is prepared|
|[Reference_Month](#reference_month)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`|Month, for which the declaration is prepared|
|[Goods_Flow_Direction](#goods_flow_direction)|`nvarchar` Allowed: `A`, `D`|The flow direction of the goods. A=Arrival, D=Dispatch|
|[Declaration_Function](#declaration_function)|`nvarchar` Allowed: `R`, `C`|Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective|
|[Declare_Statistical_Values](#declare_statistical_values)|`bit` |Does the declaration contain statistical values? 1=Yes; 0=No|
|[Intrastat_Declaration_Id](#intrastat_declaration_id)|`uniqueidentifier` `PK`||

## Columns

### Reference_Year


Reference_Year


Year, for which the declaration is prepared


Year, for which the declaration is prepared

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Declarations](Its_Declarations.md).[Reference_Year](Its_Declarations.md#reference_year)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Reference_Month


Reference_Month


Month, for which the declaration is prepared


Month, for which the declaration is prepared

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`|
|Default Value|None|
|Derived From|[Its_Declarations](Its_Declarations.md).[Reference_Month](Its_Declarations.md#reference_month)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Goods_Flow_Direction


Goods_Flow_Direction


The flow direction of the goods. A=Arrival, D=Dispatch


The flow direction of the goods. A=Arrival, D=Dispatch

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
|Allowed Values|`A`, `D`|
|Default Value|None|
|Derived From|[Its_Declarations](Its_Declarations.md).[Goods_Flow_Direction](Its_Declarations.md#goods_flow_direction)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Declaration_Function


Declaration_Function


Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective


Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective

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
|Allowed Values|`R`, `C`|
|Default Value|R|
|Derived From|[Its_Declarations](Its_Declarations.md).[Declaration_Function](Its_Declarations.md#declaration_function)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Declare_Statistical_Values


Declare_Statistical_Values


Does the declaration contain statistical values? 1=Yes; 0=No


Does the declaration contain statistical values? 1=Yes; 0=No

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
|Derived From|[Its_Declarations](Its_Declarations.md).[Declare_Statistical_Values](Its_Declarations.md#declare_statistical_values)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Intrastat_Declaration_Id


Intrastat_Declaration_Id

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
|Derived From|[Its_Declarations](Its_Declarations.md).[Intrastat_Declaration_Id](Its_Declarations.md#intrastat_declaration_id)|
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


