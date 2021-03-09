# Table Srv_Service_Activity_Agreed_Materials

Contains the materials, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Materials

## Owner Tables Hierarchy

* [Srv_Service_Activity_Materials](Srv_Service_Activity_Materials.md)
* [Srv_Service_Activities](Srv_Service_Activities.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Service_Activity_Material_Id](#service_activity_material_id)|`uniqueidentifier` Readonly||
|[Service_Agreement_Material_Id](#service_agreement_material_id)|`uniqueidentifier` Readonly|Service agreement material line that records the paid or agreed in advance material|
|[Agreed_Quantity](#agreed_quantity)|`decimal(18, 3)` Readonly|Quantity from the service agreement material line that is accounted for this service activity material line|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Material_Id

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


