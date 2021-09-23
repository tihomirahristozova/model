---
uid: Projects.ProjectWorkElements
---
# Projects.ProjectWorkElements Entity

**Namespace:** [Projects](Projects.md)  

Contains the work elements from the work breakdown structure, which are included in the projects. Entity: Prj_Project_Work_Elements

## Default Visualization
Default Display Text Format:  
_{Project.Name:T} : {Project.Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.Projects](Projects.Projects.md)  
Aggregate Root:  
[Projects.Projects](Projects.Projects.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.ProjectWorkElements.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Project](Projects.ProjectWorkElements.md#project) | [Projects](Projects.Projects.md) | The `Project`(Projects.ProjectWorkElements.md#project) to which this ProjectWorkElement belongs. `Required` `Filter(multi eq)` `Owner` |
| [ProjectTypeWorkElement](Projects.ProjectWorkElements.md#projecttypeworkelement) | [TypeWorkElements](Projects.TypeWorkElements.md) | The work element from the project type on which the current work element is based. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Project

The `Project`(Projects.ProjectWorkElements.md#project) to which this ProjectWorkElement belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Projects](Projects.Projects.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ProjectTypeWorkElement

The work element from the project type on which the current work element is based. `Required` `Filter(multi eq)`

_Type_: **[TypeWorkElements](Projects.TypeWorkElements.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Projects.ProjectWorkElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Projects.ProjectWorkElements erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectWorkElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectWorkElements?$top=10>

