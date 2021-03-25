---
uid: Projects.TypeWorkElements
---
# Projects.TypeWorkElements Entity

**Namespace:** [Projects](Projects.md)  

The work elements of the work breakdown structure of each project type. Entity: Prj_Type_Work_Elements

## Default Visualization
Default Display Text Format:  
_{WorkElementCode}: {WorkElementName:T}_  
Default Search Member:  
_WorkElementCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectTypes](Projects.ProjectTypes.md)  
Aggregate Root:  
[Projects.ProjectTypes](Projects.ProjectTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Projects.TypeWorkElements.md#fullpath) | string(25) (nullable) | The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `Filter(eq;like)` `ReadOnly` 
| [Id](Projects.TypeWorkElements.md#id) | guid |  
| [Notes](Projects.TypeWorkElements.md#notes) | string(2147483647) (nullable) | Notes for this TypeWorkElement. 
| [ParentFullPath](Projects.TypeWorkElements.md#parentfullpath) | string(25) (nullable) | The full path of the parent work element in this project type. null when this is root element. `Filter(eq;like)` 
| [WorkElementCode](Projects.TypeWorkElements.md#workelementcode) | string(3) | The code of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)` 
| [WorkElementName](Projects.TypeWorkElements.md#workelementname) | string(254) | The name of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TypeWorkElements.md#projecttype) | [ProjectTypes](Projects.ProjectTypes.md) | The `ProjectType`(Projects.TypeWorkElements.md#projecttype) to which this TypeWorkElement belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### FullPath

The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `Filter(eq;like)` `ReadOnly`

_Type_: **string(25) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this TypeWorkElement.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ParentFullPath

The full path of the parent work element in this project type. null when this is root element. `Filter(eq;like)`

_Type_: **string(25) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  

### WorkElementCode

The code of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)`

_Type_: **string(3)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **3**  

### WorkElementName

The name of the work element, unique among the sibling elements within the parent work element. `Required` `Filter(eq)`

_Type_: **string(254)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### ProjectType

The `ProjectType`(Projects.TypeWorkElements.md#projecttype) to which this TypeWorkElement belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProjectTypes](Projects.ProjectTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TypeWorkElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TypeWorkElements erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TypeWorkElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TypeWorkElements?$top=10>

