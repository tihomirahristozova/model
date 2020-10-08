---
uid: Finance.Cost.Templates
---
# Finance.Cost.Templates

Cost templates specify how to calculate and allocate costs. Entity: Cost_Templates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.Templates.md#Id) | guid |  
| [CostTemplateCode](Finance.Cost.Templates.md#CostTemplateCode) | string | Unique code of the cost template. [Required] [Filter(eq)] 
| [CostTemplateName](Finance.Cost.Templates.md#CostTemplateName) | string | Name of the cost template. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Cost.Templates.md#Currency) | [General.Currencies](General.Currencies.md) | The currency of the calculations, based on the template. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| CostTypes | [Finance.Cost.TemplateCostTypes](Finance.Cost.TemplateCostTypes.md) | List of [TemplateCostType](Finance.Cost.TemplateCostTypes.md) child objects, based on the [Finance.Cost.TemplateCostType.CostTemplate](Finance.Cost.TemplateCostTypes.md#CostTemplate) back reference 
| Levels | [Finance.Cost.TemplateLevels](Finance.Cost.TemplateLevels.md) | List of [TemplateLevel](Finance.Cost.TemplateLevels.md) child objects, based on the [Finance.Cost.TemplateLevel.CostTemplate](Finance.Cost.TemplateLevels.md#CostTemplate) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CostTemplateCode

> Unique code of the cost template. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### CostTemplateName

> Name of the cost template. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### Currency

> The currency of the calculations, based on the template. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.Templates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.Templates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.Templates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_Templates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_Templates?$top=10>

