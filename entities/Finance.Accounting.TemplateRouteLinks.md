---
uid: Finance.Accounting.TemplateRouteLinks
---
# Finance.Accounting.TemplateRouteLinks Entity

When specified denotes that another route uses the template, initially bound to one route. Entity: Acc_Template_Route_Links

Default Display Text Format:  
_{Route.ProcedureName:T}_  
Default Search Member:  
_Route.ProcedureName_  

Aggregate Parent:  
[Systems.Workflow.Routes](Systems.Workflow.Routes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.TemplateRouteLinks.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Finance.Accounting.TemplateRouteLinks.md#route) | [Routes](Systems.Workflow.Routes.md) | Route for which the specified template will be activated. [Required] [Filter(multi eq)] [Owner] |
| [Template](Finance.Accounting.TemplateRouteLinks.md#template) | [Templates](Finance.Accounting.Templates.md) | Template that will be activated for the specified route. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Route

Route for which the specified template will be activated. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Template

Template that will be activated for the specified route. [Required] [Filter(multi eq)]

_Type_: **[Templates](Finance.Accounting.Templates.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.TemplateRouteLinks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.TemplateRouteLinks erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_TemplateRouteLinks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_TemplateRouteLinks?$top=10>

