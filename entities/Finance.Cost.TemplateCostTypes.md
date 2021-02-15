---
uid: Finance.Cost.TemplateCostTypes
---
# Finance.Cost.TemplateCostTypes Entity

Contains the cost types and their hierachy positions within a cost calculation. Entity: Cost_Template_Cost_Types

Default Display Text Format:  
_{CostTemplate.CostTemplateCode}: {CostTemplate.CostTemplateName:T}_  
Default Search Member:  
_CostTemplate.CostTemplateCode_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [HierarchyLevel](Finance.Cost.TemplateCostTypes.md#hierarchylevel) | int32 | The level in the hierarchy on which this cost is incurred (0..9). [Required] [Filter(ge;le)] 
| [Id](Finance.Cost.TemplateCostTypes.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostTemplate](Finance.Cost.TemplateCostTypes.md#costtemplate) | [Templates](Finance.Cost.Templates.md) | The [Template](Finance.Cost.Templates.md) to which this TemplateCostType belongs. [Required] [Filter(multi eq)] [Owner] |
| [CostType](Finance.Cost.TemplateCostTypes.md#costtype) | [CostTypes](Finance.Cost.CostTypes.md) | The Cost Type for which the hierarchy is specified. [Required] [Filter(multi eq)] |


## Attribute Details

### HierarchyLevel

The level in the hierarchy on which this cost is incurred (0..9). [Required] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### CostTemplate

The [Template](Finance.Cost.Templates.md) to which this TemplateCostType belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Templates](Finance.Cost.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CostType

The Cost Type for which the hierarchy is specified. [Required] [Filter(multi eq)]

_Type_: **[CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.TemplateCostTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.TemplateCostTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_TemplateCostTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_TemplateCostTypes?$top=10>

