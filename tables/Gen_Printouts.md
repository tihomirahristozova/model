# Table Gen_Printouts

Contains data about binding of printout layouts to specific user-defined document types. Entity: Gen_Printouts

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Printout_Id](#printout_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(64)` |The application which stored and uses the printout|
|[Printout_Name](#printout_name)|`nvarchar(64)` |The name of the printout. Unique within the application form|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type to which this printout layout is bound.|
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` |The printout layout, that is bound to the document type.|
|[Definition_Format](#definition_format)|`nvarchar(16)` |Obsolete. Not used.|
|[Definition](#definition)|`nvarchar(1073741823)` |Obsolete. Not used.|
|[Is_Default](#is_default)|`bit` |1 if this is the default printout for the application form|
|[Ord](#ord)|`int` |Order in the list of printouts when using direct printing|
|[Copies](#copies)|`int` |Number of copies that should be printed when using direct printing|
|[Report_Id](#report_id)|`uniqueidentifier` |If not NULL points to a custom report that indicates which data will be loaded in the printout.|
|[Backward_Compatibility](#backward_compatibility)|`bit` |Obsolete. Not used.|
|[Allow_Printing_On_State](#allow_printing_on_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`|The user can print documents only with state equal or greater than Allow_Printing_On_State|
|[Ord_Priority](#ord_priority)|`int` |Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command.|
|[Ord_Filter_Xml](#ord_filter_xml)|`nvarchar(2147483647)` |The condition, required to be matched in order for the printout to be executed upon "Print All" command.|
|[Notes](#notes)|`nvarchar(512)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Printout_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Printout_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Printout_Layout_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Definition_Format

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Definition

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Ord

| Property | Value |
| - | - |
|Type|int|

### Copies

| Property | Value |
| - | - |
|Type|int|

### Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Backward_Compatibility

| Property | Value |
| - | - |
|Type|bit|

### Allow_Printing_On_State

| Property | Value |
| - | - |
|Type|smallint|

### Ord_Priority

| Property | Value |
| - | - |
|Type|int|

### Ord_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


