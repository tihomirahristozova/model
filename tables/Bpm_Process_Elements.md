# Table Bpm_Process_Elements

Contains the flow elements of the process model. Entity: Bpm_Process_Elements

## Owner Tables Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Element_Id](#process_element_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this element belongs.|
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` |The process lane to which this element belongs.|
|[Process_Element_Code](#process_element_code)|`nvarchar(16)` |Element code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Element_Name](#process_element_name)|`nvarchar(512)` `ML`|Multilanguage process name.|
|[Element_Type](#element_type)|`nvarchar(1)` Allowed: `A`, `E`, `G`, `C`|Basic type of the element. A=Activity; E=Event; G=Gateway; C=Artifact.|
|[Element_Subtype](#element_subtype)|`nvarchar(3)` Allowed: `ATU`, `ATM`, `ATV`, `ATC`, `ATB`, `ATS`, `ATR`, `ES1`, `ES2`, `ES4`, `EE1`, `EE2`, `EE5`, `EE9`, `EI1`, `EI2`, `EI3`, `EI4`, `GEX`, `GIN`, `CAT`, `CGP`|Subtype of the element. Each type allows only certain types of sub-types.|
|[Instructions_Html](#instructions_html)|`nvarchar(2147483647)` |Detailed instructions to the executor in HTML format.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Lane_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Element_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Process_Element_Name

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Element_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Element_Subtype

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Instructions_Html

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


