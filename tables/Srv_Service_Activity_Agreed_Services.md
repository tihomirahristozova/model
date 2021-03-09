# Table Srv_Service_Activity_Agreed_Services

Contains the services, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Services

## Owner Tables Hierarchy

* [Srv_Service_Activity_Services](Srv_Service_Activity_Services.md)
* [Srv_Service_Activities](Srv_Service_Activities.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Service_Activity_Service_Id](#service_activity_service_id)|`uniqueidentifier` Readonly||
|[Service_Agreement_Service_Id](#service_agreement_service_id)|`uniqueidentifier` Readonly|Service agreement service line that records the paid or agreed in advance service or product|
|[Agreed_Quantity](#agreed_quantity)|`decimal(18, 3)` Readonly|Quantity from the service agreement service line that is accounted for this service activity service line|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Agreed_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


