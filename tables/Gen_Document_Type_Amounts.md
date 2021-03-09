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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### User_Can_Change_Input

| Property | Value |
| - | - |
|Type|bit|

### Required_From_Date

| Property | Value |
| - | - |
|Type|date|

### Required_Thru_Date

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


