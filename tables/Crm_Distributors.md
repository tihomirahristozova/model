# Table Crm_Distributors

Distributors are external for the enterprise persons or companies who obtain sales orders from end-customers in benefit of the enterprise. Entity: Crm_Distributors

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Distributor_Id](#distributor_id)|`uniqueidentifier` `PK`|Unique distributor Id|
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Flat_Commision_Percentage](#flat_commision_percentage)|`decimal(7, 6)` |Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressive/qunatity considerations|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Distributor_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Flat_Commision_Percentage

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


