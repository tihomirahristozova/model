# Table Cm_Activity_Resources

Contains the resources, allocated to the activities. Entity: Cm_Activity_Resources

# Aggregate Hierarchy

* [Cm_Activities](Cm_Activities.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Activity_Resource_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this ActivityResource. |
|Resource_Usage_Percent|`Decimal`||The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)` |
