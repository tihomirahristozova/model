# Table Log_Transportation_Execution_Lines

Contains details of executions of transportation order lines. Entity: Log_Transportation_Execution_Lines (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Log_Transportation_Executions](Log_Transportation_Executions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Execution_Line_Id](#transportation_execution_line_id)|`uniqueidentifier` `PK`||
|[Transportation_Execution_Id](#transportation_execution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number within this execution.|
|[Execution_Of_Transportation_Order_Line_Id](#execution_of_transportation_order_line_id)|`uniqueidentifier` |The transportation order line, which is executed.|
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` |The geographic point, where the operation is executed.|
|[Operation_Type](#operation_type)|`nvarchar(1)` Allowed: `L`, `U`, `O`|The type of operation being executed. L=Loading; U=Unloading; O=Other.|
|[Pallets_Count](#pallets_count)|`int` |Number of pallets affected by this operation. NULL when unknown or N/A.|
|[Weight_Kg](#weight_kg)|`int` |Cargo weight in kg, affected by this operation. NULL when unknown or N/A.|
|[Volume_Cbm](#volume_cbm)|`int` |Cargo volume in cubic meters, affected by this operation. NULL when unknown or N/A.|
|[Execution_Date](#execution_date)|`date` |The date when the operation was executed.|
|[Execution_Time](#execution_time)|`time` |The time when the operation was executed.|
|[Pallet_Number](#pallet_number)|`nvarchar(32)` |Pallet number, when applicable. NULL when unknown or not applicable.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Transportation_Execution_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transportation_Execution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Execution_Of_Transportation_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Pallets_Count

| Property | Value |
| - | - |
|Type|int|

### Weight_Kg

| Property | Value |
| - | - |
|Type|int|

### Volume_Cbm

| Property | Value |
| - | - |
|Type|int|

### Execution_Date

| Property | Value |
| - | - |
|Type|date|

### Execution_Time

| Property | Value |
| - | - |
|Type|time|

### Pallet_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


