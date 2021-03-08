# Table Fleet_Vehicle_Location_History_Records

Stores information about vehicle locations. Entity: Fleet_Vehicle_Location_History_Records

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Location_History_Record_Id|`Guid`|`PK`, Readonly||
|Current_Speed_KmH|`Int32?`||The current speed of the vehicle in km/h. null means the speed is unknown. `Introduced in version 19.1` |
|Latitude|`Decimal`||Latitude of the vehicle at the specified time. Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range `-90, 90`. `Required` |
|Longitude|`Decimal`||Longitude of the vehicle at the specified time. Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range `-180, 180`. `Required` |
|Time|`DateTime`||The time, for which the location is stored. `Required` |
