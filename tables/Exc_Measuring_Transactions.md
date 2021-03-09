# Table Exc_Measuring_Transactions

Transaction of product input or output, measured with specialized measuring device for excise purposes. Entity: Exc_Measuring_Transactions (Introduced in version 21.1.1.9)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Measuring_Transaction_Id](#measuring_transaction_id)|`uniqueidentifier` `PK`||
|[Tax_Warehouse_Id](#tax_warehouse_id)|`uniqueidentifier` |The tax warehouse, where the transaction occurred.|
|[Measuring_Device_Code](#measuring_device_code)|`nvarchar(32)` |The code of the measuring device, used to measure the transaction.|
|[Transaction_Number](#transaction_number)|`nvarchar(32)` |Transaction number, unique for the measuring device.|
|[Direction](#direction)|`nvarchar(1)` Allowed: `I`, `O`|The direction of the transaction - IN/OUT.|
|[Start_Time_Utc](#start_time_utc)|`datetime` |Starting time of the transaction (in UTC time).|
|[End_Time_Utc](#end_time_utc)|`datetime` |Ending time of the transaction (in UTC time).|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which was being measured.|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity of the product, measured with this transaction.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Alcohol_Degree](#alcohol_degree)|`int` |For alcoholic products, contains the percentage of pure alcohol. NULL when the transaction is not for alcoholic products.|
|[Alcohol_Temperature](#alcohol_temperature)|`int` |For alcoholic products, contains the temperature of the fluid, when Alcohol Degree was calculated. The measurement unit is dependent on the national regulation (usually Celsius). NULL for non-alcoholic products.|
|[Alcohol_Density](#alcohol_density)|`int` |For alcoholic products, contains the average density for the whole transaction. The measurement unit is dependent on the applicable legislation. NULL for non-alcoholic products.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Measuring_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tax_Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Measuring_Device_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Transaction_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Start_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### End_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Alcohol_Degree

| Property | Value |
| - | - |
|Type|int|

### Alcohol_Temperature

| Property | Value |
| - | - |
|Type|int|

### Alcohol_Density

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


