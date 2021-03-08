# Table Geo_Map_Points

Geographical map points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Geo_Map_Points

# Aggregate Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Map_Point_Id|`Guid`|`PK`, Readonly||
|Address|`String`||The descriptive physical address, related to this map point. |
|Latitude|`Decimal`||Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range `-90, 90`. `Required` `Default(0)` |
|Longitude|`Decimal`||Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range `-180, 180`. `Required` `Default(0)` |
|Map_Point_Name|`MultilanguageString`||Map point short name (Multilanguage). `Required` `Filter(eq;like)` |
