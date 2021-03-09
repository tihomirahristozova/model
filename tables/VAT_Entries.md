# Table VAT_Entries

Contains the entries in the VAT sales and purchase ledgers. Entity: VAT_Entries

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Entry_Id](#entry_id)|`uniqueidentifier` `PK`|Unique identification number of this VAT entry.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Entry_Type](#entry_type)|`nvarchar(1)` Allowed: `P`, `S`|Type of the VAT entry. S=Sales, P=Purchases.|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type that caused this entry.|
|[Party_Id](#party_id)|`uniqueidentifier` |The corresponding party that is involved in the operation that caused this entry.|
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar(16)` |VAT number by registration (or national number) for the party specified by Party_Id.|
|[Registration_Number](#registration_number)|`nvarchar(16)` |Identification code (IC) for the party specified by Party_Id.|
|[Referenced_Document_Type_Id](#referenced_document_type_id)|`uniqueidentifier` |Type of the document that represents the operation that caused this entry.|
|[Referenced_Document_No](#referenced_document_no)|`nvarchar(20)` |Number of the document that represents the operation that caused this entry.|
|[Amount_Base](#amount_base)|`decimal(14, 2)` |Amount of the operation without the tax in base currency.|
|[VAT_Amount_Base](#vat_amount_base)|`decimal(14, 2)` |The amount of the tax for the operation in base currency.|
|[Apply_Date](#apply_date)|`date` |Specifies the date on which the entry should be applied in the reporting. Usually equal to the document date with exception for documents that are late to be applied in the correct period|
|[Cash_Reporting_Mode](#cash_reporting_mode)|`bit` |When true, specifies, that the special cash reporting mode should be used for VAT reporting. When false, the normal (classic) VAT reporting is used.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Entry_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entry_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Referenced_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Referenced_Document_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### VAT_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Apply_Date

| Property | Value |
| - | - |
|Type|date|

### Cash_Reporting_Mode

| Property | Value |
| - | - |
|Type|bit|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


