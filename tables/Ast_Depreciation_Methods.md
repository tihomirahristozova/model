# Table Ast_Depreciation_Methods

Depreciation methods. Contains both system-defined and user-defined methods. Entity: Ast_Depreciation_Methods

## Summary

| Name | Type | Description |
| - | - | --- |
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` `PK`||
|[Depreciation_Method_Name](#depreciation_method_name)|`nvarchar(254)` ||
|[Depreciation_Function](#depreciation_function)|`nvarchar(3)` Allowed: `FAC`, `STL`, `SYD`, `TAB`|Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table|
|[Factor](#factor)|`decimal(5, 3)` |Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor|
|[Months_In_A_Period](#months_in_a_period)|`int` |Number of equal valued months calculated with single application of the function|
|[Start_From_Next_Month](#start_from_next_month)|`bit` |When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month.|
|[Is_System](#is_system)|`bit` Readonly|Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user.|
|[Period_Determination_Method](#period_determination_method)|`nvarchar(2)` Allowed: `NM`, `CM`, `BD`|Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Depreciation_Method_Id


Depreciation_Method_Id

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
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Depreciation_Method_Id](Ast_Depreciation_Methods.md#depreciation_method_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Depreciation_Method_Name


Depreciation_Method_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Depreciation_Method_Name](Ast_Depreciation_Methods.md#depreciation_method_name)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Depreciation_Function


Depreciation_Function


Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table


Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table

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
|Allowed Values|`FAC`, `STL`, `SYD`, `TAB`|
|Default Value|STL|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Depreciation_Function](Ast_Depreciation_Methods.md#depreciation_function)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Factor


Factor


Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor


Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor

| Property | Value |
| - | - |
|Type|decimal(5, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Factor](Ast_Depreciation_Methods.md#factor)|
|Format|N3|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Months_In_A_Period


Months_In_A_Period


Number of equal valued months calculated with single application of the function


Number of equal valued months calculated with single application of the function

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|12|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Months_In_A_Period](Ast_Depreciation_Methods.md#months_in_a_period)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Start_From_Next_Month


Start_From_Next_Month


When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month.


When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Start_From_Next_Month](Ast_Depreciation_Methods.md#start_from_next_month)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_System


Is_System


Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user.


Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Is_System](Ast_Depreciation_Methods.md#is_system)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Period_Determination_Method


Period_Determination_Method


Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days


Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days

| Property | Value |
| - | - |
|Type|nvarchar(2)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`NM`, `CM`, `BD`|
|Default Value|None|
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Period_Determination_Method](Ast_Depreciation_Methods.md#period_determination_method)|
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
|Max Length|2|
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
|Derived From|[Ast_Depreciation_Methods](Ast_Depreciation_Methods.md).[Row_Version](Ast_Depreciation_Methods.md#row_version)|
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


