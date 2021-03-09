# Table Log_Transportation_Orders

Transportation ordered to specific carrier or vehicle. Entity: Log_Transportation_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Order_Id](#transportation_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Departure_Date](#departure_date)|`date` |Planned departure date.|
|[Departure_Time](#departure_time)|`time` |Planned departure time.|
|[Arrival_Date](#arrival_date)|`date` |Planned arrival date.|
|[Arrival_Time](#arrival_time)|`time` |Planned arrival time.|
|[Transportation_Mode_Id](#transportation_mode_id)|`uniqueidentifier` |The mode of transportation which should be used for this order. NULL when it is unknown or doesn't matter.|
|[Carrier_Id](#carrier_id)|`uniqueidentifier` |The carrier chosen for this transportation. NULL when the transportation is done with own transport.|
|[Transportation_Vehicle_Id](#transportation_vehicle_id)|`uniqueidentifier` |The own transportation vehicle, which will be used for the transportation.|
|[From_Geo_Point_Id](#from_geo_point_id)|`uniqueidentifier` |The geographic point from which the route begins.|
|[To_Geo_Point_Id](#to_geo_point_id)|`uniqueidentifier` |The geographic point at which the route ends.|
|[Row_Version](#row_version)|`timestamp` ||
|[Crew_Id](#crew_id)|`uniqueidentifier` |The crew which is assigned to operate the vehicle of the current Transportation Order. If null means the crew is yet unknown or the order is executed by external carrier.|

## Columns

### Transportation_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Departure_Date

| Property | Value |
| - | - |
|Type|date|

### Departure_Time

| Property | Value |
| - | - |
|Type|time|

### Arrival_Date

| Property | Value |
| - | - |
|Type|date|

### Arrival_Time

| Property | Value |
| - | - |
|Type|time|

### Transportation_Mode_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Carrier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transportation_Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Crew_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


