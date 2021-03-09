# Table Gen_Document_Type_Properties

Default user-defined properties, which should be added to new documents. Entity: Gen_Document_Type_Properties

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Property_Id](#user_property_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, for which to add user-defined properties.|
|[Line_No](#line_no)|`int` |Line number, unique within the document type|
|[Property_Id](#property_id)|`uniqueidentifier` |The user-defined property, which should be added.|
|[Default_Property_Value](#default_property_value)|`nvarchar(254)` |The default value of the property when creating new documents.|
|[Default_Property_Value_Description](#default_property_value_description)|`nvarchar(254)` `ML`|Default description value of the property when creating new documents.|
|[Required](#required)|`bit` |1 if the property is required when creating documents of this type|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not null, specifies that the current rule is valid only for the specified company.|
|[Required_From_Date](#required_from_date)|`datetime` |When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date.|
|[Required_Thru_Date](#required_thru_date)|`datetime` |When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date.|
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` |Internal Id of the default value of the property.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### User_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Default_Property_Value_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Required

| Property | Value |
| - | - |
|Type|bit|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Required_Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


