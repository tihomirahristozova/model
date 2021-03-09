# Table Rent_Transaction_Lines

Contains all transactions of Record of Handover / Handing-Over Record lines. Entity: Rent_Transaction_Lines

## Owner Tables Hierarchy

* [Rent_Transactions](Rent_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rent_Transaction_Line_Id](#rent_transaction_line_id)|`uniqueidentifier` `PK`||
|[Rent_Transaction_Id](#rent_transaction_id)|`uniqueidentifier` ||
|[Rental_Asset_Id](#rental_asset_id)|`uniqueidentifier` |Rental asset|
|[Transaction_Type](#transaction_type)|`nvarchar(1)` Allowed: `D`, `R`, `W`, `S`|Transaction Type|
|[Lease_Contract_Id](#lease_contract_id)|`uniqueidentifier` |Lease Contract|
|[Lessee_Customer_Id](#lessee_customer_id)|`uniqueidentifier` |Lessee Customer|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Transaction Timestamp|
|[Notes](#notes)|`nvarchar(2147483647)` |Notes|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rent_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rent_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Id

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


