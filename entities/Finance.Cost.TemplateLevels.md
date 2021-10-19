---
uid: Finance.Cost.TemplateLevels
---
# Finance.Cost.TemplateLevels Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Represents named hierarchy levels within a cost calculation. The hierarchy levels are used to specify cost allocation mechanisms. Entity: Cost_Template_Levels

## Default Visualization
Default Display Text Format:  
_{LevelName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Cost.Templates](Finance.Cost.Templates.md)  
Aggregate Root:  
[Finance.Cost.Templates](Finance.Cost.Templates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [HierarchyLevel](Finance.Cost.TemplateLevels.md#hierarchylevel) | int32 | The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9). `Required` `Default(0)` `Filter(ge;le)` 
| [Id](Finance.Cost.TemplateLevels.md#id) | guid |  
| [LevelName](Finance.Cost.TemplateLevels.md#levelname) | string (254) | The name of the hierarchy level. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostTemplate](Finance.Cost.TemplateLevels.md#costtemplate) | [Templates](Finance.Cost.Templates.md) | The `Template`(Finance.Cost.Templates.md) to which this TemplateLevel belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### HierarchyLevel

The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9). `Required` `Default(0)` `Filter(ge;le)`

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LevelName

The name of the hierarchy level. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### CostTemplate

The `Template`(Finance.Cost.Templates.md) to which this TemplateLevel belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Templates](Finance.Cost.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Cost.TemplateLevels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.TemplateLevels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_TemplateLevels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_TemplateLevels?$top=10>

