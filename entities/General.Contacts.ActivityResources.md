---
uid: General.Contacts.ActivityResources
---
# General.Contacts.ActivityResources Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Contains the resources, allocated to the activities. Entity: Cm_Activity_Resources

## Default Visualization
Default Display Text Format:  
_{Activity.DocumentType.TypeName:T} {Activity.DocumentNo}_  
Default Search Member:  
_Activity.DocumentType.TypeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Activities](General.Contacts.Activities.md)  
Aggregate Root:  
[General.Contacts.Activities](General.Contacts.Activities.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.ActivityResources.md#id) | guid |  
| [Notes](General.Contacts.ActivityResources.md#notes) | string (255) __nullable__ | Notes for this ActivityResource. 
| [ResourceUsagePercent](General.Contacts.ActivityResources.md#resourceusagepercent) | decimal (18, 4) | The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Activity](General.Contacts.ActivityResources.md#activity) | [Activities](General.Contacts.Activities.md) | The `Activity`(General.Contacts.ActivityResources.md#activity) to which this ActivityResource belongs. `Required` `Filter(multi eq)` `Owner` |
| [Resource](General.Contacts.ActivityResources.md#resource) | [Resources](General.Resources.Resources.md) | The resource, which is required by the activity. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ActivityResource.

_Type_: **string (255) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **255**  

### ResourceUsagePercent

The planned resource usage for this activity in percents (100% = 1). Values of more than 100% are allowed when more than 1 resource is required. `Required` `Default(1)`

_Type_: **decimal (18, 4)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Activity

The `Activity`(General.Contacts.ActivityResources.md#activity) to which this ActivityResource belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Activities](General.Contacts.Activities.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Resource

The resource, which is required by the activity. `Required` `Filter(multi eq)`

_Type_: **[Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Contacts.ActivityResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.ActivityResources erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityResources?$top=10>

