# Table Srv_Service_Agreement_Lines

Service agreement lines represent the individual serviced objects that are covered by the service agreement. Entity: Srv_Service_Agreement_Lines

## Owner Tables Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Agreement_Object_Id](#service_agreement_object_id)|`uniqueidentifier` `PK`||
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Service_Object_Id](#service_object_id)|`uniqueidentifier` |The service object, which is covered by the current agreement.|
|[Quantity](#quantity)|`decimal(14, 3)` |The quantity of the service object that is included in the agreement|
|[Service_Type_Id](#service_type_id)|`uniqueidentifier` |The type (level) of service that is agreed|
|[Line_Start_Date_Time](#line_start_date_time)|`datetime` |The starting date and time of the agreement coverage for the current line.|
|[Line_End_Date_Time](#line_end_date_time)|`datetime` |The ending date and time of the agreement coverage for the current line.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Agreement_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(14, 3)|

### Service_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Line_End_Date_Time

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


