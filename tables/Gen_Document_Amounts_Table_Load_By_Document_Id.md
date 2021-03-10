# Procedure Gen_Document_Amounts_Table_Load_By_Document_Id


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Id](#document_amount_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The type of the amount.|
|[Input_Percent](#input_percent)|`decimal(7, 6)` |When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type).|
|[Input_Amount](#input_amount)|`decimal(14, 2)` |When not null, specifies directly the amount of the additional amount.|
|[Input_Amount_Currency_Id](#input_amount_currency_id)|`uniqueidentifier` |When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null.|
|[User_Can_Change_Input](#user_can_change_input)|`bit` |1 if the user, entering the document is allowed to change the default input percent|
|[Input_Unit_Amount](#input_unit_amount)|`decimal(14, 5)` |Input unit amount for the calculation of the current amount.|
|[Input_Unit_Id](#input_unit_id)|`uniqueidentifier` |Measurement unit of the input unit amount.|
|[Row_Version](#row_version)|`timestamp` ||
|[Base_Amount](#base_amount)|`decimal(0, 0)` Readonly|The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet.|
|[Total_Distributed_Amount](#total_distributed_amount)|`decimal(0, 0)` Readonly|The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet.|
|[Amount_Type_Code](#amount_type_code)|`nvarchar` Readonly||
|[Description](#description)|`nvarchar` Readonly||

## Columns

### Document_Amount_Id


Document_Amount_Id

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
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Document_Amount_Id](Gen_Document_Amounts.md#document_amount_id)|
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

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Document_Id](Gen_Document_Amounts.md#document_id)|
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

### Document_Amount_Type_Id


Document_Amount_Type_Id


The type of the amount.


The type of the amount.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Document_Amount_Type_Id](Gen_Document_Amounts.md#document_amount_type_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Input_Percent


Input_Percent


When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type).


When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type).

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
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Input_Percent](Gen_Document_Amounts.md#input_percent)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Input_Amount


Input_Amount


When not null, specifies directly the amount of the additional amount.


When not null, specifies directly the amount of the additional amount.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Input_Amount](Gen_Document_Amounts.md#input_amount)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Input_Amount_Currency_Id


Input_Amount_Currency_Id


When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null.


When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Input_Amount_Currency_Id](Gen_Document_Amounts.md#input_amount_currency_id)|
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
|Equals|NULL|yes|yes|

### User_Can_Change_Input


User_Can_Change_Input


1 if the user, entering the document is allowed to change the default input percent


1 if the user, entering the document is allowed to change the default input percent

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
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[User_Can_Change_Input](Gen_Document_Amounts.md#user_can_change_input)|
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

### Input_Unit_Amount


Input_Unit_Amount


Input unit amount for the calculation of the current amount.


Input unit amount for the calculation of the current amount.

| Property | Value |
| - | - |
|Type|decimal(14, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Input_Unit_Amount](Gen_Document_Amounts.md#input_unit_amount)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|

### Input_Unit_Id


Input_Unit_Id


Measurement unit of the input unit amount.


Measurement unit of the input unit amount.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Input_Unit_Id](Gen_Document_Amounts.md#input_unit_id)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Row_Version](Gen_Document_Amounts.md#row_version)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Base_Amount


Base_Amount


The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet.


The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Base_Amount](Gen_Document_Amounts.md#base_amount)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Total_Distributed_Amount


Total_Distributed_Amount


The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet.


The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amounts](Gen_Document_Amounts.md).[Total_Distributed_Amount](Gen_Document_Amounts.md#total_distributed_amount)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Amount_Type_Code


Amount_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md).[Amount_Type_Code](Gen_Document_Amount_Types.md#amount_type_code)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Description


Description

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
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
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|


