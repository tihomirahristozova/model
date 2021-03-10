# Table Prd_Work_Order_Document_Types_Options

Options for user-defined Work Order document types. Entity: Prd_Work_Order_Document_Types_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Work_Order_Document_Types_Option_Id](#work_order_document_types_option_id)|`uniqueidentifier` `PK`|Option for user-defined Work Order document type|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |User-defined Work Order document type|
|[Completing_Output_Order_Document_Type_Id](#completing_output_order_document_type_id)|`uniqueidentifier` |User-defined Completing Output Order document type|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Work_Order_Document_Types_Option_Id


Work_Order_Document_Types_Option_Id


Option for user-defined Work Order document type


Option for user-defined Work Order document type

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
|Derived From|[Prd_Work_Order_Document_Types_Options](Prd_Work_Order_Document_Types_Options.md).[Work_Order_Document_Types_Option_Id](Prd_Work_Order_Document_Types_Options.md#work_order_document_types_option_id)|
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


User-defined Work Order document type


User-defined Work Order document type

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Document_Types_Options](Prd_Work_Order_Document_Types_Options.md).[Document_Type_Id](Prd_Work_Order_Document_Types_Options.md#document_type_id)|
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

### Completing_Output_Order_Document_Type_Id


Completing_Output_Order_Document_Type_Id


User-defined Completing Output Order document type


User-defined Completing Output Order document type

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Work_Order_Document_Types_Options](Prd_Work_Order_Document_Types_Options.md).[Completing_Output_Order_Document_Type_Id](Prd_Work_Order_Document_Types_Options.md#completing_output_order_document_type_id)|
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
|Derived From|[Prd_Work_Order_Document_Types_Options](Prd_Work_Order_Document_Types_Options.md).[Row_Version](Prd_Work_Order_Document_Types_Options.md#row_version)|
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


