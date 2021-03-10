# Table Its_Document_Amount_Type_Settings

Specifies the additional amounts, which are added to the invoiced and statistical values. Entity: Its_Document_Amount_Type_Settings

## Owner Tables Hierarchy

* [Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Setting_Id](#document_amount_type_setting_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the setting is valid|
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The amount type which will be added to the invoiced or the statistical value|
|[Add_To_Invoiced_Value](#add_to_invoiced_value)|`bit` |1= to add the amount to the invoiced value, 0=otherwise|
|[Add_To_Statistical_Value](#add_to_statistical_value)|`bit` |1= to add the amount to the statistical value, 0=otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Type_Setting_Id


Document_Amount_Type_Setting_Id

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
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Document_Amount_Type_Setting_Id](Its_Document_Amount_Type_Settings.md#document_amount_type_setting_id)|
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
|Equals|NULL|no|yes|

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company for which the setting is valid


The enterprise company for which the setting is valid

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Enterprise_Company_Id](Its_Document_Amount_Type_Settings.md#enterprise_company_id)|
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

### Document_Amount_Type_Id


Document_Amount_Type_Id


The amount type which will be added to the invoiced or the statistical value


The amount type which will be added to the invoiced or the statistical value

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Document_Amount_Type_Id](Its_Document_Amount_Type_Settings.md#document_amount_type_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Add_To_Invoiced_Value


Add_To_Invoiced_Value


1= to add the amount to the invoiced value, 0=otherwise


1= to add the amount to the invoiced value, 0=otherwise

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
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Add_To_Invoiced_Value](Its_Document_Amount_Type_Settings.md#add_to_invoiced_value)|
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

### Add_To_Statistical_Value


Add_To_Statistical_Value


1= to add the amount to the statistical value, 0=otherwise


1= to add the amount to the statistical value, 0=otherwise

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
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Add_To_Statistical_Value](Its_Document_Amount_Type_Settings.md#add_to_statistical_value)|
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
|Derived From|[Its_Document_Amount_Type_Settings](Its_Document_Amount_Type_Settings.md).[Row_Version](Its_Document_Amount_Type_Settings.md#row_version)|
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


