# Table Crm_Dealers

External dealers. Entity: Crm_Dealers

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Dealer_Id](#dealer_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` |The base party record of the dealer|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which this dealer is recorded|
|[From_Date](#from_date)|`datetime` |Start of the dealer relationship|
|[Thru_Date](#thru_date)|`datetime` |Termination date of the dealership. NULL for active dealers|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


