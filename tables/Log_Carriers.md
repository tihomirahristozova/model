# Table Log_Carriers

Represents a carrier agreement. One actual carrier can have different agreements over time or with different enterprise companies. Entity: Log_Carriers

## Summary

| Name | Type | Description |
| - | - | --- |
|[Carrier_Id](#carrier_id)|`uniqueidentifier` `PK`||
|[Code](#code)|`nvarchar(16)` |Unique carrier code (or call sign). The code is unique within all enterprise companies.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which signed the carrier agreement.|
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier contract with the carrier.|
|[Is_Active](#is_active)|`bit` |Specifies whether the carrier agreement is active.|
|[Agreement_Start_Date](#agreement_start_date)|`date` |The start date of the agreement with this carrier.|
|[Agreement_End_Date](#agreement_end_date)|`date` |The ending date of the agreement with this carrier. NULL for agreements which are still active.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Carrier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Agreement_Start_Date

| Property | Value |
| - | - |
|Type|date|

### Agreement_End_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


