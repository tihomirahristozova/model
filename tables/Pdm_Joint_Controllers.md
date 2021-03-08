# Table Pdm_Joint_Controllers

Contains relationship between process and joint controllers. For processes with control role, these are the joint controllers. Otherwise, these are the joint controllers, on behalf of which the enterprise company processes the data. Entity: Pdm_Joint_Controllers (Introduced in version 18.2)

# Aggregate Hierarchy

* [Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Joint_Controller_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Should usually contain a short description of the role of the joint controller. |
