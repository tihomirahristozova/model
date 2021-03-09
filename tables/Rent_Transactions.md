# Table Rent_Transactions

Contains all transactions of Record of Handover / Handing-Over Record . Entity: Rent_Transactions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rent_Transaction_Id](#rent_transaction_id)|`uniqueidentifier` `PK`|Rent Transaction PK|
|[Document_Id](#document_id)|`uniqueidentifier` |Document Id|
|[Transaction_Type](#transaction_type)|`nvarchar(1)` Allowed: `D`, `R`, `W`, `S`|Transaction Type|
|[Lease_Contract_Id](#lease_contract_id)|`uniqueidentifier` |Lease Contract|
|[Lessee_Customer_Id](#lessee_customer_id)|`uniqueidentifier` |Lessee Customer|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Transaction Timestamp|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rent_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Lease_Contract_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lessee_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

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


