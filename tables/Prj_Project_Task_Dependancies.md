# Table Prj_Project_Task_Dependancies

Represents dependancy between project tasks. Entity: Prj_Project_Task_Dependancies

# Aggregate Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Task_Dependancy_Id|`Guid`|`PK`, Readonly||
|Dependancy_Type|`DependancyType`|Allowed: `FS`, `SS`, `FF`, `SF`, `SY`|FS=Finish-to-Start;SS=Start-to-Start;FF=Finish-to-Finish;SF=Start-to-Finish;SY=Sync (all types in the same time). `Required` `Default("FS")` |
