# Table Prj_Project_Task_Resources

Contains the resources, required by the project tasks. Entity: Prj_Project_Task_Resources

## Owner Tables Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Resource_Id](#project_task_resource_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The task for which the resource is planned.|
|[Resource_Id](#resource_id)|`uniqueidentifier` |The planned resource.|
|[Resource_Usage_Percent](#resource_usage_percent)|`decimal(18, 4)` |The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Resource_Usage_Hours](#resource_usage_hours)|`decimal(10, 2)` |The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage.|
|[Cost_Per_Hour](#cost_per_hour)|`decimal(12, 5)` |Cost per hour for the resource usage for this task (in the currency of the project).|
|[Task_Total_Cost](#task_total_cost)|`decimal(14, 2)` |Total cost for this task (in the currency of the project).|
|[Billing_Price_Per_Hour](#billing_price_per_hour)|`decimal(12, 5)` |When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. NULL means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price|
|[Billing_Total_Amount](#billing_total_amount)|`decimal(14, 2)` |When not NULL, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). NULL means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour.|
|[Per_Use_Cost](#per_use_cost)|`decimal(14, 2)` |One time cost for each resource usage, specified in the projects currency.|
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` |The concrete resource instance, which should be used. NULL when no specific resource instance is required.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Resource_Id


Project_Task_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Project_Task_Resource_Id](Prj_Project_Task_Resources.md#project_task_resource_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Project_Task_Id


Project_Task_Id


The task for which the resource is planned.


The task for which the resource is planned.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prj_Project_Tasks](Prj_Project_Tasks.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Project_Task_Id](Prj_Project_Task_Resources.md#project_task_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Id


Resource_Id


The planned resource.


The planned resource.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Resources](Gen_Resources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Resource_Id](Prj_Project_Task_Resources.md#resource_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Usage_Percent


Resource_Usage_Percent


The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required.


The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required.

| Property | Value |
| - | - |
|Type|decimal(18, 4)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|1|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Resource_Usage_Percent](Prj_Project_Task_Resources.md#resource_usage_percent)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Notes](Prj_Project_Task_Resources.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Resource_Usage_Hours


Resource_Usage_Hours


The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage.


The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage.

| Property | Value |
| - | - |
|Type|decimal(10, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Resource_Usage_Hours](Prj_Project_Task_Resources.md#resource_usage_hours)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Cost_Per_Hour


Cost_Per_Hour


Cost per hour for the resource usage for this task (in the currency of the project).


Cost per hour for the resource usage for this task (in the currency of the project).

| Property | Value |
| - | - |
|Type|decimal(12, 5)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Cost_Per_Hour](Prj_Project_Task_Resources.md#cost_per_hour)|
|Format|N2|
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Task_Total_Cost


Task_Total_Cost


Total cost for this task (in the currency of the project).


Total cost for this task (in the currency of the project).

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Task_Total_Cost](Prj_Project_Task_Resources.md#task_total_cost)|
|Format|N2|
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Billing_Price_Per_Hour


Billing_Price_Per_Hour


When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. NULL means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price


When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. NULL means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price

| Property | Value |
| - | - |
|Type|decimal(12, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Billing_Price_Per_Hour](Prj_Project_Task_Resources.md#billing_price_per_hour)|
|Format|N2|
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Billing_Total_Amount


Billing_Total_Amount


When not NULL, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). NULL means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour.


When not NULL, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). NULL means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Billing_Total_Amount](Prj_Project_Task_Resources.md#billing_total_amount)|
|Format|N2|
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Per_Use_Cost


Per_Use_Cost


One time cost for each resource usage, specified in the projects currency.


One time cost for each resource usage, specified in the projects currency.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Per_Use_Cost](Prj_Project_Task_Resources.md#per_use_cost)|
|Format|N2|
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Resource_Instance_Id


Resource_Instance_Id


The concrete resource instance, which should be used. NULL when no specific resource instance is required.


The concrete resource instance, which should be used. NULL when no specific resource instance is required.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Resource_Instances](Gen_Resource_Instances.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Resource_Instance_Id](Prj_Project_Task_Resources.md#resource_instance_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prj_Project_Task_Resources](Prj_Project_Task_Resources.md).[Row_Version](Prj_Project_Task_Resources.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


