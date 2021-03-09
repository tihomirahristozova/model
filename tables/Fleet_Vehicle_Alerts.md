# Table Fleet_Vehicle_Alerts

Contains alerts, specific to one vehicle. Alerts are created based on many sources and stay active, until excplicitly hidden. Entity: Fleet_Vehicle_Alerts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Alert_Id](#vehicle_alert_id)|`uniqueidentifier` `PK`||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The vehicle, for which is the alert.|
|[Time](#time)|`datetime` |The time of the alert.|
|[Source](#source)|`nvarchar(1)` |The source of the alert. G=GPS, O=OBD, M=Maintenance.|
|[Alert_Type](#alert_type)|`nvarchar(3)` |The type of the alert. The type is specfic to the Source.|
|[Description](#description)|`nvarchar(254)` |Description of the alert (Multilanguage).|
|[Is_Hidden](#is_hidden)|`bit` |Specifies, whether the alert is hidden (e.g. managed by the responsible person).|

## Columns

### Vehicle_Alert_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time

| Property | Value |
| - | - |
|Type|datetime|

### Source

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Alert_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Hidden

| Property | Value |
| - | - |
|Type|bit|


