# Table Rent_Transaction_Templates

Specifies additional options for document routes, generating Rental Transactions. Entity: Rent_Transaction_Templates

## Summary

| Name | Type | Description |
| - | - | --- |
|[Rent_Transaction_Template_Id](#rent_transaction_template_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |The route for which the transaction template is defined.|
|[Transaction_Type](#transaction_type)|`nvarchar(1)` Allowed: `D`, `R`, `W`, `S`||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Rent_Transaction_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


