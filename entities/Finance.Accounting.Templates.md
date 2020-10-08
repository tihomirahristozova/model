---
uid: Finance.Accounting.Templates
---
# Finance.Accounting.Templates

Accounting templates are used to automate the postings for repetitive business transactions. Templates can be bound to almost all documents and automate their postings. Entity: Acc_Templates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.Templates.md#id) | guid |  
| [Name](Finance.Accounting.Templates.md#name) | string | The name of this Template. [Required] [Filter(like)] 
| [VoucherDateSource](Finance.Accounting.Templates.md#voucherdatesource) | string (nullable) | Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual. 
| [VoucherDescriptionMask](Finance.Accounting.Templates.md#voucherdescriptionmask) | string (nullable) | Template voucher description. Can use field substitutes, surrounded with square brackets. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Finance.Accounting.Templates.md#route) | [Systems.Workflow.Routes](Systems.Workflow.Routes.md) | The route which activates the template. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [Finance.Accounting.TemplateLines](Finance.Accounting.TemplateLines.md) | List of [TemplateLine](Finance.Accounting.TemplateLines.md) child objects, based on the [Finance.Accounting.TemplateLine.Template](Finance.Accounting.TemplateLines.md#template) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this Template. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### VoucherDateSource

> Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoucherDescriptionMask

> Template voucher description. Can use field substitutes, surrounded with square brackets.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Route

> The route which activates the template. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Workflow.Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.Templates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.Templates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.Templates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_Templates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_Templates?$top=10>

