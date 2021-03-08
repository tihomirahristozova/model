# Table Prj_Project_Task_Resources

Contains the resources, required by the project tasks. Entity: Prj_Project_Task_Resources

# Aggregate Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Project_Task_Resource_Id|`Guid`|`PK`, Readonly||
|Billing_Price_Per_Hour|`Decimal?`||When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. null means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price. `Filter(eq)` |
|Billing_Total_Amount|`Decimal?`||When not null, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). null means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour. `Filter(eq)` |
|Cost_Per_Hour|`Decimal`||Cost per hour for the resource usage for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)` |
|Notes|`String`||Notes for this ProjectTaskResource. |
|Resource_Usage_Hours|`Decimal`||The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage. `Required` `Default(0)` `Filter(eq)` |
|Resource_Usage_Percent|`Decimal`||The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)` `Filter(eq)` |
|Task_Total_Cost|`Decimal`||Total cost for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)` |
