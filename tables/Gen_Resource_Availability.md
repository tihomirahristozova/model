# Table Gen_Resource_Availability

Contains the resources availability for the different periods. Each period is a separate record. The availability of a resource for any given date is determined by the sum of all availability periods that include it. Entity: Gen_Resource_Availability

# Aggregate Hierarchy

* [Gen_Resources](Gen_Resources.md)
* [Gen_Resource_Groups](Gen_Resource_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Resource_Availability_Id|`Guid`|`PK`, Readonly||
|Available_Resources|`Decimal`||The quantity of the resource, available for the specified period. For non-discrete resources, this number can contain fractions. When several availability periods for a resource overlap, the total availability is the sum of all. `Required` `Default(1)` |
|From_Date|`DateTime`||The date from which availability starts. `Required` |
|To_Date|`DateTime?`||The date to which the availability continues. When null, the availability continues infinitely. |
