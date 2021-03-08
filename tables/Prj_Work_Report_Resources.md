# Table Prj_Work_Report_Resources

Each record contains usage of resource, reported by the related Work Report. Entity: Prj_Work_Report_Resources

# Aggregate Hierarchy

* [Prj_Work_Reports](Prj_Work_Reports.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Work_Report_Resource_Id|`Guid`|`PK`, Readonly||
|Actual_End_Time|`DateTime?`||Optionally, specifies the actual date and time when the resource usage ended. `Filter(eq;like)` |
|Actual_Start_Time|`DateTime?`||Optionally, specifies the actual date and time when the resource usage began. `Filter(eq;like)` |
|Total_Resource_Usage_Hours|`Decimal`||The total number of resource-hours, which are actually consumed. Equals to the duration of the task, multiplied by the average resource usage. `Required` `Default(0)` `Filter(eq;like)` |
