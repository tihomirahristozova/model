# Table Log_Transportation_Requisitions

Client requisition for transportation. Entity: Log_Transportation_Requisitions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Requisition_Id](#transportation_requisition_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Requested_Departure_Date](#requested_departure_date)|`date` |Requested date of departure. NULL when no specific date is requested.|
|[Requested_Departure_Time](#requested_departure_time)|`time` |Requested time of departure. NULL when no specific time is requested.|
|[Requested_Arrival_Date](#requested_arrival_date)|`date` |Requested arrival date. NULL when no specific date is requested.|
|[Requested_Arrival_Time](#requested_arrival_time)|`time` |Requested arrival time. NULL when no specific time is requested.|
|[Transport_From_Party_Id](#transport_from_party_id)|`uniqueidentifier` |Shipping party.|
|[Transport_From_Party_Contact_Mechanism_Id](#transport_from_party_contact_mechanism_id)|`uniqueidentifier` |Loading address.|
|[Transport_From_Geo_Point_Id](#transport_from_geo_point_id)|`uniqueidentifier` |Geographical location of the loading, if available.|
|[Transport_To_Party_Id](#transport_to_party_id)|`uniqueidentifier` |Receiving party.|
|[Transport_To_Party_Contact_Mechanism_Id](#transport_to_party_contact_mechanism_id)|`uniqueidentifier` |Unload address.|
|[Transport_To_Geo_Point_Id](#transport_to_geo_point_id)|`uniqueidentifier` |Geographical location of the unloading, if available.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requested_Departure_Date

| Property | Value |
| - | - |
|Type|date|

### Requested_Departure_Time

| Property | Value |
| - | - |
|Type|time|

### Requested_Arrival_Date

| Property | Value |
| - | - |
|Type|date|

### Requested_Arrival_Time

| Property | Value |
| - | - |
|Type|time|

### Transport_From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_From_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_From_Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_To_Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


