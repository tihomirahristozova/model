# Table Gen_Document_Type_Amounts

Specifies amount types, that should be automatically added to documents of a given type. Entity: Gen_Document_Type_Amounts

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_Amount_Id](#document_type_amount_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the amount type is specified|
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The amount type that should be automatically added to the documents of the specified type|
|[Default_Percent](#default_percent)|`decimal(7, 6)` |Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type|
|[User_Can_Change_Input](#user_can_change_input)|`bit` |1 if the user, entering the document is allowed to change the default input percent|
|[Required_From_Date](#required_from_date)|`date` |When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date.|
|[Required_Thru_Date](#required_thru_date)|`date` |When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Type_Amount_Id


Document_Type_Amount_Id

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
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Document_Type_Amount_Id](Gen_Document_Type_Amounts.md#document_type_amount_id)|
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


The document type for which the amount type is specified


The document type for which the amount type is specified

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Document_Type_Id](Gen_Document_Type_Amounts.md#document_type_id)|
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

### Document_Amount_Type_Id


Document_Amount_Type_Id


The amount type that should be automatically added to the documents of the specified type


The amount type that should be automatically added to the documents of the specified type

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
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Document_Amount_Type_Id](Gen_Document_Type_Amounts.md#document_amount_type_id)|
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
|Equals|NULL|no|no|

### Default_Percent


Default_Percent


Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type


Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type

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
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Default_Percent](Gen_Document_Type_Amounts.md#default_percent)|
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
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[User_Can_Change_Input](Gen_Document_Type_Amounts.md#user_can_change_input)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Required_From_Date


Required_From_Date


When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date.


When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Required_From_Date](Gen_Document_Type_Amounts.md#required_from_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Required_Thru_Date


Required_Thru_Date


When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date.


When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Required_Thru_Date](Gen_Document_Type_Amounts.md#required_thru_date)|
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
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Gen_Document_Type_Amounts](Gen_Document_Type_Amounts.md).[Row_Version](Gen_Document_Type_Amounts.md#row_version)|
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


