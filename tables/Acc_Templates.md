# Table Acc_Templates

Accounting templates are used to automate the postings for repetitive business transactions. Templates can be bound to almost all documents and automate their postings. Entity: Acc_Templates

## Owner Tables Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Template_Id](#template_id)|`uniqueidentifier` `PK`||
|[Template_Name](#template_name)|`nvarchar(254)` ||
|[Route_Id](#route_id)|`uniqueidentifier` |The route which activates the template|
|[Voucher_Date_Source](#voucher_date_source)|`nvarchar(2000)` |Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual.|
|[Voucher_Description_Mask](#voucher_description_mask)|`nvarchar(2147483647)` |Template voucher description. Can use field substitutes, surrounded with square brackets|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Template_Id


Template_Id

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
|Derived From|[Acc_Templates](Acc_Templates.md).[Template_Id](Acc_Templates.md#template_id)|
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

### Template_Name


Template_Name

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
|Derived From|[Acc_Templates](Acc_Templates.md).[Template_Name](Acc_Templates.md#template_name)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Route_Id


Route_Id


The route which activates the template


The route which activates the template

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Wf_Routes](Wf_Routes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Templates](Acc_Templates.md).[Route_Id](Acc_Templates.md#route_id)|
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

### Voucher_Date_Source


Voucher_Date_Source


Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual.


Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual.

| Property | Value |
| - | - |
|Type|nvarchar(2000)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Acc_Templates](Acc_Templates.md).[Voucher_Date_Source](Acc_Templates.md#voucher_date_source)|
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
|Max Length|2000|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Voucher_Description_Mask


Voucher_Description_Mask


Template voucher description. Can use field substitutes, surrounded with square brackets


Template voucher description. Can use field substitutes, surrounded with square brackets

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
|Derived From|[Acc_Templates](Acc_Templates.md).[Voucher_Description_Mask](Acc_Templates.md#voucher_description_mask)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
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
|Derived From|[Acc_Templates](Acc_Templates.md).[Row_Version](Acc_Templates.md#row_version)|
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


