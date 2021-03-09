# Table Log_Transportation_Modes

Represents a mode of transportation, like water, air, road, etc. Entity: Log_Transportation_Modes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Mode_Id](#transportation_mode_id)|`uniqueidentifier` `PK`||
|[Transportation_Mode_Code](#transportation_mode_code)|`nvarchar(8)` |Unique transportation mode code.|
|[Transportation_Mode_Name](#transportation_mode_name)|`nvarchar(254)` |Multilanguage name of the mode of transportation.|
|[System_Icon](#system_icon)|`nvarchar(1)` |Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Mode_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transportation_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(8)|

### Transportation_Mode_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### System_Icon

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


