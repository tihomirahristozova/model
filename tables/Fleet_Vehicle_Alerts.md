# Table Fleet_Vehicle_Alerts

Contains alerts, specific to one vehicle. Alerts are created based on many sources and stay active, until excplicitly hidden. Entity: Fleet_Vehicle_Alerts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Alert_Id|`Guid`|`PK`, Readonly||
|Alert_Type|`String`||The type of the alert. The type is specfic to the Source. `Required` |
|Description|`String`||Description of the alert (Multilanguage). `Required` |
|Is_Hidden|`Boolean`||Specifies, whether the alert is hidden (e.g. managed by the responsible person). `Required` `Default(false)` |
|Source|`String`||The source of the alert. G=GPS, O=OBD, M=Maintenance. `Required` |
|Time|`DateTime`||The time of the alert. `Required` `ORD` |
