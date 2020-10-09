---
uid: General.Contacts.ActivityResources
---
# General.Contacts.ActivityResources

Contains the resources, allocated to the activities. Entity: Cm_Activity_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.ActivityResources.md#id) | guid |  
| [Notes](General.Contacts.ActivityResources.md#notes) | string (nullable) | Notes for this ActivityResource. 
| [ResourceUsagePercent](General.Contacts.ActivityResources.md#resourceusagepercent) | decimal | The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](General.Contacts.ActivityResources.md#activity) | [Activities](General.Contacts.Activities.md) | The [Activity](General.Contacts.ActivityResources.md#activity) to which this ActivityResource belongs. [Required] [Filter(multi eq)] [Owner] |
| [Resource](General.Contacts.ActivityResources.md#resource) | [Resources](General.Resources.Resources.md) | The resource, which is required by the activity. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ActivityResource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResourceUsagePercent

> The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Activity

> The [Activity](General.Contacts.ActivityResources.md#activity) to which this ActivityResource belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Activities](General.Contacts.Activities.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

> The resource, which is required by the activity. [Required] [Filter(multi eq)]

_Type_: **[Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.ActivityResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ActivityResources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.ActivityResources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityResources?$top=10>

