---
uid: Projects.TypeWorkElements
---
# Projects.TypeWorkElements

The work elements of the work breakdown structure of each project type. Entity: Prj_Type_Work_Elements

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TypeWorkElements.md#Id) | guid |  
| [FullPath](Projects.TypeWorkElements.md#FullPath) | string (nullable) | The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. [Filter(eq;like)] [ReadOnly] 
| [Notes](Projects.TypeWorkElements.md#Notes) | string (nullable) | Notes for this TypeWorkElement. 
| [ParentFullPath](Projects.TypeWorkElements.md#ParentFullPath) | string (nullable) | The full path of the parent work element in this project type. null when this is root element. [Filter(eq;like)] 
| [WorkElementCode](Projects.TypeWorkElements.md#WorkElementCode) | string | The code of the work element, unique among the sibling elements within the parent work element. [Required] [Filter(eq)] 
| [WorkElementName](Projects.TypeWorkElements.md#WorkElementName) | string | The name of the work element, unique among the sibling elements within the parent work element. [Required] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectType](Projects.TypeWorkElements.md#ProjectType) | [Projects.ProjectTypes](Projects.ProjectTypes.md) | The [ProjectType](Projects.TypeWorkElements.md#ProjectType) to which this TypeWorkElement belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FullPath

> The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. [Filter(eq;like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this TypeWorkElement.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentFullPath

> The full path of the parent work element in this project type. null when this is root element. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### WorkElementCode

> The code of the work element, unique among the sibling elements within the parent work element. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### WorkElementName

> The name of the work element, unique among the sibling elements within the parent work element. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### ProjectType

> The [ProjectType](Projects.TypeWorkElements.md#ProjectType) to which this TypeWorkElement belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectTypes](Projects.ProjectTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Projects.TypeWorkElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TypeWorkElements erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.TypeWorkElements erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TypeWorkElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TypeWorkElements?$top=10>

