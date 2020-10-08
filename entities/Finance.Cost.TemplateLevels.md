---
uid: Finance.Cost.TemplateLevels
---
# Finance.Cost.TemplateLevels

Represents named hierarchy levels within a cost calculation. The hierarchy levels are used to specify cost allocation mechanisms. Entity: Cost_Template_Levels

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.TemplateLevels.md#Id) | guid |  
| [HierarchyLevel](Finance.Cost.TemplateLevels.md#HierarchyLevel) | int32 | The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9). [Required] [Default(0)] [Filter(ge;le)] 
| [LevelName](Finance.Cost.TemplateLevels.md#LevelName) | string | The name of the hierarchy level. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostTemplate](Finance.Cost.TemplateLevels.md#CostTemplate) | [Finance.Cost.Templates](Finance.Cost.Templates.md) | The [Template](Finance.Cost.Templates.md) to which this TemplateLevel belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### HierarchyLevel

> The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9). [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### LevelName

> The name of the hierarchy level. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### CostTemplate

> The [Template](Finance.Cost.Templates.md) to which this TemplateLevel belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Templates](Finance.Cost.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.TemplateLevels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.TemplateLevels erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.TemplateLevels erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_TemplateLevels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_TemplateLevels?$top=10>

