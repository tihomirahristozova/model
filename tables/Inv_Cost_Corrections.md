# Table Inv_Cost_Corrections

Cost corrections provide a way to correct the cost of stock transactions after they are issued. Entity: Inv_Cost_Corrections

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Correction_Id](#cost_correction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Source_Transaction_Id](#source_transaction_id)|`uniqueidentifier` Readonly|Transaction that determines which transactions need cost correction. The corrected transactions are those that depend on the specified cost in the source transaction.|
|[Corrected_Transaction_Id](#corrected_transaction_id)|`uniqueidentifier` Readonly|Transaction that is corrected with this cost correction|
|[From_Date](#from_date)|`datetime` |The date from which to start looking for transactions, needing cost correction. It is used only when the source transaction is NULL.|
|[Thru_Date](#thru_date)|`datetime` |The date at which to stop looking for transactions, needing cost correction. It is used only when the source transaction is NULL.|
|[IsValid](#isvalid)|`bit` |Obsolete. Not used. (Should be set to 1 if the document is completed and not void. Required for the indexed view Inv_Cost_Corrections_Summary, because Gen_Documents_Table cannot be included in the view)|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Correction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Source_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Corrected_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### IsValid

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


