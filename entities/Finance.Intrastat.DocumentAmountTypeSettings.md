---
uid: Finance.Intrastat.DocumentAmountTypeSettings
---
# Finance.Intrastat.DocumentAmountTypeSettings

Specifies the additional amounts, which are added to the invoiced and statistical values. Entity: Its_Document_Amount_Type_Settings

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Intrastat.DocumentAmountTypeSettings.md#Id) | guid |  
| [AddToInvoicedValue](Finance.Intrastat.DocumentAmountTypeSettings.md#AddToInvoicedValue) | boolean | True= to add the amount to the invoiced value, false=otherwise. [Required] [Default(false)] 
| [AddToStatisticalValue](Finance.Intrastat.DocumentAmountTypeSettings.md#AddToStatisticalValue) | boolean | True= to add the amount to the statistical value, false=otherwise. [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](Finance.Intrastat.DocumentAmountTypeSettings.md#DocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount type which will be added to the invoiced or the statistical value. [Required] [Filter(multi eq)] [Owner] |
| [EnterpriseCompany](Finance.Intrastat.DocumentAmountTypeSettings.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the setting is valid. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AddToInvoicedValue

> True= to add the amount to the invoiced value, false=otherwise. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AddToStatisticalValue

> True= to add the amount to the statistical value, false=otherwise. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DocumentAmountType

> The amount type which will be added to the invoiced or the statistical value. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The enterprise company for which the setting is valid. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Intrastat.DocumentAmountTypeSettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Intrastat.DocumentAmountTypeSettings erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Intrastat.DocumentAmountTypeSettings erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_DocumentAmountTypeSettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_DocumentAmountTypeSettings?$top=10>

