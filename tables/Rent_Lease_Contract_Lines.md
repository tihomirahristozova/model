# Table Rent_Lease_Contract_Lines

The detail lines of rental contracts. Each line contains rental conditions for one asset of the rental contract. Entity: Rent_Lease_Contract_Lines

## Owner Tables Hierarchy

* [Rent_Lease_Contracts](Rent_Lease_Contracts.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Lease_Line_Id](#lease_line_id)|`uniqueidentifier` `PK`||
|[Lease_Contract_Id](#lease_contract_id)|`uniqueidentifier` ||
|[Rental_Asset_Id](#rental_asset_id)|`uniqueidentifier` |The asset which is rented with the current contract.|
|[Start_Date](#start_date)|`date` |Starting date of lease for this asset|
|[End_Date](#end_date)|`date` |Ending date of lease of this asset|
|[Line_Notes](#line_notes)|`nvarchar(2147483647)` |Notes for this line.|
|[Guarantee_Amount](#guarantee_amount)|`decimal(14, 2)` ||
|[Line_No](#line_no)|`int` |Consecutive number of the line within the lease contract.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Lease_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lease_Contract_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Id

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

### Line_Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Guarantee_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


