# Table Gen_Geo_Points

Geographical (geo) points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Gen_Geo_Points

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Geo_Point_Id|`Guid`|`PK`, Readonly||
|Address|`String`||The descriptive physical address, related to this geo point. `Filter(eq;like)` |
|Latitude|`Decimal`||Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range `-90, 90`. `Required` `Default(0)` `Filter(eq;ge;le)` |
|Longitude|`Decimal`||Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range `-180, 180`. `Required` `Default(0)` `Filter(eq;ge;le)` |
|Geo_Point_Name|`MultilanguageString`||Geo point short name (Multilanguage). `Required` `Filter(eq;like)` |
