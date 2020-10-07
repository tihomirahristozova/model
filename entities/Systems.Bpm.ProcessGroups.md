# Systems.Bpm.ProcessGroups

Represents a node in the hierarchy of process groups. Entity: Bpm_Process_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessGroups.md#Id) | guid |  
| [Notes](Systems.Bpm.ProcessGroups.md#Notes) | string (nullable) | Notes for this ProcessGroup. 
| [Code](Systems.Bpm.ProcessGroups.md#Code) | string | Group code, unique within the parent group. [Required] [Filter(eq;like)] 
| [Name](Systems.Bpm.ProcessGroups.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Multilanguage process group name. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Systems.Bpm.ProcessGroups.md#Parent) | [Systems.Bpm.ProcessGroups](Systems.Bpm.ProcessGroups.md) (nullable) | Parent process group in the hierarchy. null means this is a root group. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ProcessGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Group code, unique within the parent group. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Multilanguage process group name. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> Parent process group in the hierarchy. null means this is a root group. [Filter(multi eq)]

_Type_: **[Systems.Bpm.ProcessGroups](Systems.Bpm.ProcessGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Bpm_Process_Groups?$top=10>

