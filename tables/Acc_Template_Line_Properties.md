# Table Acc_Template_Line_Properties

Contains the way to obtain the values for each required property of both the debit and the credit accounts. Entity: Acc_Template_Line_Properties

## Owner Tables Hierarchy

* [Acc_Template_Lines](Acc_Template_Lines.md)
* [Acc_Templates](Acc_Templates.md)
* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Is_Debit](#is_debit)|`bit` |If Is_Debit=1 then this property is for the debit account in the template line for which is this record. If Is_Debit=0 then the property is for the credit account.|
|[Property_No](#property_no)|`int` |The ordinal position of the property value in the item key of the account.|
|[Property_Id](#property_id)|`uniqueidentifier` |The property which value will be included in the item key of the account.|
|[Property_Value_Source_Type](#property_value_source_type)|`nvarchar(64)` |Type of source for the property value. For example: System properties, User properties for document, Constant, ...|
|[Property_Value_Source](#property_value_source)|`nvarchar(2000)` |Source for the property value according to the chosen source type.|
|[Template_Line_Property_Id](#template_line_property_id)|`uniqueidentifier` `PK`||
|[Template_Line_Id](#template_line_id)|`uniqueidentifier` ||
|[Property_Description](#property_description)|`nvarchar(254)` `ML`|Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant)|
|[Constant_Value_Id](#constant_value_id)|`uniqueidentifier` |The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Is_Debit

| Property | Value |
| - | - |
|Type|bit|

### Property_No

| Property | Value |
| - | - |
|Type|int|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Value_Source_Type

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Property_Value_Source

| Property | Value |
| - | - |
|Type|nvarchar(2000)|

### Template_Line_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Template_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Constant_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


