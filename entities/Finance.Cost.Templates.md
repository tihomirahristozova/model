---
uid: Finance.Cost.Templates
---
# Finance.Cost.Templates Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Cost templates specify how to calculate and allocate costs. Entity: Cost_Templates

## Default Visualization
Default Display Text Format:  
_{CostTemplateCode}: {CostTemplateName:T}_  
Default Search Member:  
_CostTemplateCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Cost.Templates](Finance.Cost.Templates.md)  
  * [Finance.Cost.TemplateCostTypes](Finance.Cost.TemplateCostTypes.md)  
  * [Finance.Cost.TemplateLevels](Finance.Cost.TemplateLevels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CostTemplateCode](Finance.Cost.Templates.md#costtemplatecode) | string | Unique code of the cost template. [Required] [Filter(eq)] 
| [CostTemplateName](Finance.Cost.Templates.md#costtemplatename) | string | Name of the cost template. [Required] [Filter(like)] 
| [Id](Finance.Cost.Templates.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Cost.Templates.md#currency) | [Currencies](General.Currencies.md) | The currency of the calculations, based on the template. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| CostTypes | [TemplateCostTypes](Finance.Cost.TemplateCostTypes.md) | List of [TemplateCostType](Finance.Cost.TemplateCostTypes.md) child objects, based on the [Finance.Cost.TemplateCostType.CostTemplate](Finance.Cost.TemplateCostTypes.md#costtemplate) back reference 
| Levels | [TemplateLevels](Finance.Cost.TemplateLevels.md) | List of [TemplateLevel](Finance.Cost.TemplateLevels.md) child objects, based on the [Finance.Cost.TemplateLevel.CostTemplate](Finance.Cost.TemplateLevels.md#costtemplate) back reference 


## Attribute Details

### CostTemplateCode

Unique code of the cost template. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### CostTemplateName

Name of the cost template. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Currency

The currency of the calculations, based on the template. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.Templates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.Templates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_Templates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_Templates?$top=10>

