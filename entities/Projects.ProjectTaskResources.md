---
uid: Projects.ProjectTaskResources
---
# Projects.ProjectTaskResources Entity

**Namespace:** [Projects](Projects.md)  

Contains the resources, required by the project tasks. Entity: Prj_Project_Task_Resources

## Default Visualization
Default Display Text Format:  
_{ProjectTask.TaskName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectTasks](Projects.ProjectTasks.md)  
Aggregate Root:  
[Projects.ProjectTasks](Projects.ProjectTasks.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BillingPricePerHour](Projects.ProjectTaskResources.md#billingpriceperhour) | decimal (12, 5) __nullable__ | When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. null means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price. `Filter(eq)` 
| [BillingTotalAmount](Projects.ProjectTaskResources.md#billingtotalamount) | decimal (14, 2) __nullable__ | When not null, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). null means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour. `Filter(eq)` 
| [CostPerHour](Projects.ProjectTaskResources.md#costperhour) | decimal (12, 5) | Cost per hour for the resource usage for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)` 
| [Id](Projects.ProjectTaskResources.md#id) | guid |  
| [Notes](Projects.ProjectTaskResources.md#notes) | string (254) __nullable__ | Notes for this ProjectTaskResource. 
| [PerUseCost](Projects.ProjectTaskResources.md#perusecost) | [Amount (14, 2)](../data-types.md#amount) __nullable__ | One time cost for each resource usage, specified in the projects currency. `Currency: ProjectTask.Project.BudgetingCurrency` 
| [ResourceUsageHours](Projects.ProjectTaskResources.md#resourceusagehours) | decimal (10, 2) | The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage. `Required` `Default(0)` `Filter(eq)` 
| [ResourceUsagePercent](Projects.ProjectTaskResources.md#resourceusagepercent) | decimal (18, 4) | The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)` `Filter(eq)` 
| [TaskTotalCost](Projects.ProjectTaskResources.md#tasktotalcost) | decimal (14, 2) | Total cost for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTask](Projects.ProjectTaskResources.md#projecttask) | [ProjectTasks](Projects.ProjectTasks.md) | The task for which the resource is planned. `Required` `Filter(multi eq)` `Owner` |
| [Resource](Projects.ProjectTaskResources.md#resource) | [Resources](General.Resources.Resources.md) | The planned resource. `Required` `Filter(multi eq)` |
| [ResourceInstance](Projects.ProjectTaskResources.md#resourceinstance) | [ResourceInstances](General.Resources.ResourceInstances.md) (nullable) | The concrete resource instance, which should be used. null when no specific resource instance is required. `Filter(multi eq)` |


## Attribute Details

### BillingPricePerHour

When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. null means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price. `Filter(eq)`

_Type_: **decimal (12, 5) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.BillingTotalAmount != null) AndAlso ( obj.BillingPricePerHour != null)), null, obj.BillingPricePerHour)`
### BillingTotalAmount

When not null, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). null means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour. `Filter(eq)`

_Type_: **decimal (14, 2) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.BillingTotalAmount != null) AndAlso ( obj.BillingPricePerHour != null)), null, obj.BillingTotalAmount)`
### CostPerHour

Cost per hour for the resource usage for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)`

_Type_: **decimal (12, 5)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.PerUseCost != null) AndAlso ( obj.ResourceUsageHours != 0)), ( ( obj.TaskTotalCost - obj.PerUseCost.Value) / obj.ResourceUsageHours), obj.CostPerHour)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ProjectTaskResource.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### PerUseCost

One time cost for each resource usage, specified in the projects currency. `Currency: ProjectTask.Project.BudgetingCurrency`

_Type_: **[Amount (14, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResourceUsageHours

The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage. `Required` `Default(0)` `Filter(eq)`

_Type_: **decimal (10, 2)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ProjectTask != null), ( obj.ProjectTask.PlannedDurationHours * obj.ResourceUsagePercent), obj.ResourceUsageHours)`
### ResourceUsagePercent

The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)` `Filter(eq)`

_Type_: **decimal (18, 4)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **1**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ProjectTask.PlannedDurationHours == 0), 0, ( obj.ResourceUsageHours / obj.ProjectTask.PlannedDurationHours))`
### TaskTotalCost

Total cost for this task (in the currency of the project). `Required` `Default(0)` `Filter(eq)`

_Type_: **decimal (14, 2)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`( ( obj.ResourceUsageHours * obj.CostPerHour) + obj.PerUseCost.Value)`

_Front-End Recalc Expressions:_  
`IIF( ( obj.PerUseCost != null), ( ( obj.ResourceUsageHours * obj.CostPerHour) + obj.PerUseCost.Value), obj.TaskTotalCost)`

## Reference Details

### ProjectTask

The task for which the resource is planned. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Resource

The planned resource. `Required` `Filter(multi eq)`

_Type_: **[Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResourceInstance

The concrete resource instance, which should be used. null when no specific resource instance is required. `Filter(multi eq)`

_Type_: **[ResourceInstances](General.Resources.ResourceInstances.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Projects.ProjectTaskResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Projects.ProjectTaskResources erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTaskResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTaskResources?$top=10>

