# Procedure Inv_Transactions_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Id](#transaction_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The main document data of the transaction|
|[Is_Scrap](#is_scrap)|`bit` |0=Non-scrap; 1=Scrap operation. Only store issue operations can be scrap.|
|[Scrap_Type_Id](#scrap_type_id)|`uniqueidentifier` |Type of scrap (scrap reason). NULL if the transaction is not scrap|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which the goods are received or issued.|
|[Store_Name](#store_name)|`nvarchar` `ML`|Name of the store|
|[Store_Responsible_Party_Name](#store_responsible_party_name)|`nvarchar` `ML`|The name of the party|
|[Scrap_Type_Description](#scrap_type_description)|`nvarchar` ||
|[Issuing_Person_Id](#issuing_person_id)|`uniqueidentifier` |The person, responsible for the issuing of the document.|
|[Receiving_Person_Id](#receiving_person_id)|`uniqueidentifier` |The person, to which the document was sent.|
|[Issuing_Person_Name](#issuing_person_name)|`nvarchar` `ML`|The name of the party|
|[Receiving_Person_Name](#receiving_person_name)|`nvarchar` `ML`|The name of the party|
|[Movement_Type](#movement_type)|`nvarchar` Allowed: `I`, `R`|Transaction movement type. R=RECEIPT, I=ISSUE|
|[Cost_Source](#cost_source)|`nvarchar` Allowed: `S`, `D`, Readonly|Determines whether the cost in the transaction is taken from the store current availability (usually this is the case for issue transactions) or the cost must be specified in the transaction itself (usually for receipt transactions). S = Store, D = Document|

## Columns

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

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

### Store_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Responsible_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Scrap_Type_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Issuing_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiving_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issuing_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Receiving_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Cost_Source

| Property | Value |
| - | - |
|Type|nvarchar|


