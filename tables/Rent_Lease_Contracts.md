# Table Rent_Lease_Contracts

Contains the lease contracts for rental assets. Entity: Rent_Lease_Contracts

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Lease_Contract_Id](#lease_contract_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Lessee_Customer_Id](#lessee_customer_id)|`uniqueidentifier` |The customer record of the lessee|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the lease contract amounts|
|[Start_Date](#start_date)|`date` |Starting date of the lease contract|
|[End_Date](#end_date)|`date` |Ending date (inclusive) of the lease contract|
|[Credit_Limit_Override](#credit_limit_override)|`bit` ||
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Lease_Contract_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lessee_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### End_Date

| Property | Value |
| - | - |
|Type|date|

### Credit_Limit_Override

| Property | Value |
| - | - |
|Type|bit|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


