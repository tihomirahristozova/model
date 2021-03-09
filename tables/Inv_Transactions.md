# Table Inv_Transactions

Executed store-receipts(in) and store-issues(out). Store-issues are recorded with minus quantity. Entity: Inv_Transactions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Id](#transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The main document data of the transaction|
|[Parent_Store_Order_Id](#parent_store_order_id)|`uniqueidentifier` |The parent (generating) store order. Deprecated, use the Parent Document reference.|
|[Is_Scrap](#is_scrap)|`bit` |0=Non-scrap; 1=Scrap operation. Only store issue operations can be scrap.|
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` |Type of scrap (scrap reason). NULL if the transaction is not scrap|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which the goods are received or issued.|
|[Issuing_Person_Id](#issuing_person_id)|`uniqueidentifier` |The person, responsible for the issuing of the document.|
|[Receiving_Person_Id](#receiving_person_id)|`uniqueidentifier` |The person, to which the document was sent.|
|[Movement_Type](#movement_type)|`nvarchar(1)` Allowed: `I`, `R`|Transaction movement type. R=RECEIPT, I=ISSUE|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document amounts are recorded.|
|[Cost_Source](#cost_source)|`nvarchar(1)` Allowed: `S`, `D`, Readonly|Determines whether the cost in the transaction is taken from the store current availability (usually this is the case for issue transactions) or the cost must be specified in the transaction itself (usually for receipt transactions). S = Store, D = Document|
|[IsValid](#isvalid)|`bit` |Managed by the system and used only for integrity purposes. Do not use.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Scrap

| Property | Value |
| - | - |
|Type|bit|

### Scrap_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issuing_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Source

| Property | Value |
| - | - |
|Type|nvarchar(1)|

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


