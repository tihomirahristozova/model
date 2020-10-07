# Finance.Accounting.TemplateRouteLinks

When specified denotes that another route uses the template, initially bound to one route. Entity: Acc_Template_Route_Links

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.TemplateRouteLinks.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Finance.Accounting.TemplateRouteLinks.md#Route) | [Systems.Workflow.Routes](Systems.Workflow.Routes.md) | Route for which the specified template will be activated. [Required] [Filter(multi eq)] [Owner] |
| [Template](Finance.Accounting.TemplateRouteLinks.md#Template) | [Finance.Accounting.Templates](Finance.Accounting.Templates.md) | Template that will be activated for the specified route. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### Route

> Route for which the specified template will be activated. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Workflow.Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Template

> Template that will be activated for the specified route. [Required] [Filter(multi eq)]

_Type_: **[Finance.Accounting.Templates](Finance.Accounting.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Accounting.TemplateRouteLinks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.TemplateRouteLinks erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.TemplateRouteLinks erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_TemplateRouteLinks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_TemplateRouteLinks?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Acc_Template_Route_Links?$top=10>

