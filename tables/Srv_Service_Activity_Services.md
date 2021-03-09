# Table Srv_Service_Activity_Services

Contains the services, which were actually performed during the service activity (repair). Entity: Srv_Service_Activity_Services

## Owner Tables Hierarchy

* [Srv_Service_Activities](Srv_Service_Activities.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Service_Id](#service_id)|`uniqueidentifier` |The type of service that is conducted|
|[Service_Name](#service_name)|`nvarchar(254)` |Description of the conducted service. The description may vary (contain additional information) from the standart name of the service.|
|[Notes](#notes)|`nvarchar(254)` |Short notes for the service|
|[Quantity](#quantity)|`decimal(9, 2)` |The quantity of the service in the measurement unit of the service|
|[Performed_By_Person_Id](#performed_by_person_id)|`uniqueidentifier` |The id of the person from the enterprise company that actually performed the work|
|[Service_Activity_Service_Id](#service_activity_service_id)|`uniqueidentifier` `PK`||
|[Service_Activity_Id](#service_activity_id)|`uniqueidentifier` ||
|[Service_Object_Id](#service_object_id)|`uniqueidentifier` |The service object that was serviced. NULL means that it is unknown or N/A|
|[Covered_By_Guarantee](#covered_by_guarantee)|`bit` |True when the performed service is covered by the guarantee.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 2)|

### Performed_By_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Covered_By_Guarantee

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


