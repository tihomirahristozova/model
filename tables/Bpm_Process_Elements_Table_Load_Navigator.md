# Query Bpm_Process_Elements_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Element_Id](#process_element_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this element belongs.|
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` |The process lane to which this element belongs. NULL when the element is not categorized to any lane. Required to be set for all elements for executable processes.|
|[Process_Element_Code](#process_element_code)|`nvarchar` |Element code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Element_Name](#process_element_name)|`nvarchar` `ML`|Multilanguage process name.|
|[Element_Type](#element_type)|`nvarchar` Allowed: `A`, `E`, `G`, `C`|Basic type of the element. A=Activity; E=Event; G=Gateway; C=Artifact.|
|[Element_Subtype](#element_subtype)|`nvarchar` Allowed: `ATU`, `ATM`, `ATV`, `ATC`, `ATB`, `ATS`, `ATR`, `ES1`, `ES2`, `ES4`, `EE1`, `EE2`, `EE5`, `EE9`, `EI1`, `EI2`, `EI3`, `EI4`, `GEX`, `GIN`, `CAT`, `CGP`|Subtype of the element. Each type allows only certain types of sub-types.|
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
|Type|nvarchar|

### Process_Element_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Element_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Element_Subtype

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


