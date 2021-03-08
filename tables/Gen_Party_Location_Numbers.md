# Table Gen_Party_Location_Numbers

Location numbers for a party. Depending on the partner with which we are doing an exchange, our location number might be different. Entity: Gen_Party_Location_Numbers (Introduced in version 19.1)

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Party_Location_Number_Id|`Guid`|`PK`, Readonly||
|Location_Coding_System|`LocationCodingSystem`|Allowed: `GLN`, `INT`|The coding system for which we are defining the location number. `Required` `Default("GLN")` `Filter(multi eq)` |
|Location_Number|`String`||The location number of Party. `Required` `Filter(multi eq;like)` `ORD` |
|Partner_Location_Number|`String`||The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. null means that the location number is not dependent on the partner location number. `Filter(multi eq)` |
|Significance|`Int32`||Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance. `Required` `Default(0)` `Filter(multi eq;ge;le)` |
