# Table Gen_Sequence_Generators

Contains one or more sequence generators for each sequence. Many sequence generators for one sequence are used when the generators must be selected conditionally or when more generators are needed for parallel numbering. Entity: Gen_Sequence_Generators

## Owner Tables Hierarchy

* [Gen_Sequences](Gen_Sequences.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sequence_Generator_Id](#sequence_generator_id)|`uniqueidentifier` `PK`||
|[Sequence_Id](#sequence_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |If specified then the generator is designated for use only in documents with that Responsible_Person_Id|
|[Next_Value](#next_value)|`nvarchar(16)` |The next number that will be issued by the sequence|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Allow_Explicit_Numbering](#allow_explicit_numbering)|`bit` |Allows to assign numbers explicitely regardless of the Next_Value of the generator (Next_Value is updated if needed)|
|[Sequence_Priority](#sequence_priority)|`int` |The priority in which the sequence is used, compared to other similar sequences. Used only for sequences, for which Simultaneous Transactions=True|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sequence_Generator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sequence_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Next_Value

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Allow_Explicit_Numbering

| Property | Value |
| - | - |
|Type|bit|

### Sequence_Priority

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


