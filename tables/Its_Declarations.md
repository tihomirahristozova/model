# Table Its_Declarations

Contains the headers of the Intrastat declarations, issued by the enterprise companies. Entity: Its_Declarations

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Intrastat_Declaration_Id](#intrastat_declaration_id)|`uniqueidentifier` `PK`|Intrastat declaration id|
|[Reference_Year](#reference_year)|`smallint` |Year, for which the declaration is prepared|
|[Reference_Month](#reference_month)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`|Month, for which the declaration is prepared|
|[Goods_Flow_Direction](#goods_flow_direction)|`nvarchar(1)` Allowed: `A`, `D`|The flow direction of the goods. A=Arrival, D=Dispatch|
|[Declaration_Function](#declaration_function)|`nvarchar(1)` Allowed: `R`, `C`|Specifies whether this is a regular or corrective declaration. R=Regular, C=Corrective|
|[Declare_Statistical_Values](#declare_statistical_values)|`bit` |Does the declaration contain statistical values? 1=Yes; 0=No|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Postal_Code](#postal_code)|`nvarchar(64)` |This field contains the postal code part of the submitter’s address|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||
|[Third_Declaring_Party_Id](#third_declaring_party_id)|`uniqueidentifier` |Third declaring party, which holds the electronic signature. This is the company which submits the declaration.|
|[Authorized_Person_Id](#authorized_person_id)|`uniqueidentifier` |The authorized person who submits the intrastat declaration.|

## Columns

### Intrastat_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Year

| Property | Value |
| - | - |
|Type|smallint|

### Reference_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Goods_Flow_Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Declaration_Function

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Declare_Statistical_Values

| Property | Value |
| - | - |
|Type|bit|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Postal_Code

| Property | Value |
| - | - |
|Type|nvarchar(64)|

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

### Third_Declaring_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Authorized_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


