# Table Gen_Document_Amount_Types

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` `PK`||
|[Amount_Type_Code](#amount_type_code)|`nvarchar(16)` |A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes|
|[Amount_Type_Name](#amount_type_name)|`nvarchar(128)` `ML`|The name of the amount type.|
|[Description](#description)|`nvarchar(254)` ||
|[Amount_Input_Allowed](#amount_input_allowed)|`bit` |1 when the user is allowed to input fixed amount for distribution|
|[Percent_Input_Allowed](#percent_input_allowed)|`bit` |1 when the user is allowed to input percent of total for distribution|
|[Distribute_By](#distribute_by)|`nvarchar(20)` Allowed: `AMOUNT`, `MEASUREMENT`, `PRODUCT DEFINITION`|Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION')|
|[Default_Percent](#default_percent)|`decimal(7, 6)` |Default percent for amounts for which percent input is allowed; NULL otherwise|
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` |Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'|
|[Add_To_Customer](#add_to_customer)|`bit` |1 means that the amount will be charged to the primary customer of the document|
|[Add_To_Line](#add_to_line)|`bit` |1 means that the resulting amount will be added to the amount of each respective line|
|[Base_On_Lines](#base_on_lines)|`bit` |1 means that the percentages will be applied over lines plus dependant amounts; 0 means only dependant amounts|
|[Round_Scale](#round_scale)|`int` |The amounts should be rounded with the specified number of digits after the decimal point. NULL means to use the currency default|
|[Is_Active](#is_active)|`bit` |1 when the amount type is active for new records; 0 - otherwise|
|[Allowed_Directions](#allowed_directions)|`int` Allowed: `-1`, `0`, `1`|Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents.|
|[Unit_Amount_Input_Allowed](#unit_amount_input_allowed)|`bit` |Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Type_Id


Document_Amount_Type_Id

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Document_Amount_Type_Id](Gen_Document_Amount_Types.md#document_amount_type_id)|
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

### Amount_Type_Code


Amount_Type_Code


A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes


A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Amount_Type_Code](Gen_Document_Amount_Types.md#amount_type_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Amount_Type_Name


Amount_Type_Name


The name of the amount type.


The name of the amount type.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Amount_Type_Name](Gen_Document_Amount_Types.md#amount_type_name)|
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
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Description


Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Description](Gen_Document_Amount_Types.md#description)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Amount_Input_Allowed


Amount_Input_Allowed


1 when the user is allowed to input fixed amount for distribution


1 when the user is allowed to input fixed amount for distribution

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Amount_Input_Allowed](Gen_Document_Amount_Types.md#amount_input_allowed)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Percent_Input_Allowed


Percent_Input_Allowed


1 when the user is allowed to input percent of total for distribution


1 when the user is allowed to input percent of total for distribution

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Percent_Input_Allowed](Gen_Document_Amount_Types.md#percent_input_allowed)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Distribute_By


Distribute_By


Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION')


Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION')

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`AMOUNT`, `MEASUREMENT`, `PRODUCT DEFINITION`|
|Default Value|AMOUNT|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Distribute_By](Gen_Document_Amount_Types.md#distribute_by)|
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
|Max Length|20|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Percent


Default_Percent


Default percent for amounts for which percent input is allowed; NULL otherwise


Default percent for amounts for which percent input is allowed; NULL otherwise

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Default_Percent](Gen_Document_Amount_Types.md#default_percent)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Distribute_By_Measurement_Category_Id


Distribute_By_Measurement_Category_Id


Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'


Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Categories](Gen_Measurement_Categories.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Distribute_By_Measurement_Category_Id](Gen_Document_Amount_Types.md#distribute_by_measurement_category_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Add_To_Customer


Add_To_Customer


1 means that the amount will be charged to the primary customer of the document


1 means that the amount will be charged to the primary customer of the document

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Add_To_Customer](Gen_Document_Amount_Types.md#add_to_customer)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Add_To_Line


Add_To_Line


1 means that the resulting amount will be added to the amount of each respective line


1 means that the resulting amount will be added to the amount of each respective line

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Add_To_Line](Gen_Document_Amount_Types.md#add_to_line)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Base_On_Lines


Base_On_Lines


1 means that the percentages will be applied over lines plus dependant amounts; 0 means only dependant amounts


1 means that the percentages will be applied over lines plus dependant amounts; 0 means only dependant amounts

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Base_On_Lines](Gen_Document_Amount_Types.md#base_on_lines)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Round_Scale


Round_Scale


The amounts should be rounded with the specified number of digits after the decimal point. NULL means to use the currency default


The amounts should be rounded with the specified number of digits after the decimal point. NULL means to use the currency default

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Round_Scale](Gen_Document_Amount_Types.md#round_scale)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


1 when the amount type is active for new records; 0 - otherwise


1 when the amount type is active for new records; 0 - otherwise

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Is_Active](Gen_Document_Amount_Types.md#is_active)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Allowed_Directions


Allowed_Directions


Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents.


Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`-1`, `0`, `1`|
|Default Value|0|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Allowed_Directions](Gen_Document_Amount_Types.md#allowed_directions)|
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

### Unit_Amount_Input_Allowed


Unit_Amount_Input_Allowed


Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount.


Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount.

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Unit_Amount_Input_Allowed](Gen_Document_Amount_Types.md#unit_amount_input_allowed)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Row_Version](Gen_Document_Amount_Types.md#row_version)|
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


