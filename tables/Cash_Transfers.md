# Table Cash_Transfers

Represents one fund transfer from one payment account to another. Entity: Cash_Transfers

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transfer_Id](#transfer_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Source_Payment_Account_Id](#source_payment_account_id)|`uniqueidentifier` |The account from which to deduct the amount|
|[Destination_Payment_Account_Id](#destination_payment_account_id)|`uniqueidentifier` |The account to which to transfer the amount|
|[Source_Amount](#source_amount)|`decimal(18, 2)` |The amount to transfer in the source currency|
|[Destination_Amount](#destination_amount)|`decimal(18, 2)` |The amount in the currency of the destination account|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transfer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Source_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Destination_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Source_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Destination_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

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


