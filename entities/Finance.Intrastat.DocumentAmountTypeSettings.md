---
uid: Finance.Intrastat.DocumentAmountTypeSettings
---
# Finance.Intrastat.DocumentAmountTypeSettings Entity

**Namespace:** [Finance.Intrastat](Finance.Intrastat.md)  

Specifies the additional amounts, which are added to the invoiced and statistical values. Entity: Its_Document_Amount_Type_Settings

## Default Visualization
Default Display Text Format:  
_{DocumentAmountType.AmountTypeName:T}_  
Default Search Members:  
_DocumentAmountType.AmountTypeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentAmountTypes](General.DocumentAmountTypes.md)  
Aggregate Root:  
[General.DocumentAmountTypes](General.DocumentAmountTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AddToInvoicedValue](Finance.Intrastat.DocumentAmountTypeSettings.md#addtoinvoicedvalue) | boolean | True= to add the amount to the invoiced value, false=otherwise. `Required` `Default(false)` 
| [AddToStatisticalValue](Finance.Intrastat.DocumentAmountTypeSettings.md#addtostatisticalvalue) | boolean | True= to add the amount to the statistical value, false=otherwise. `Required` `Default(false)` 
| [Id](Finance.Intrastat.DocumentAmountTypeSettings.md#id) | guid |  
| [RowVersion](Finance.Intrastat.DocumentAmountTypeSettings.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](Finance.Intrastat.DocumentAmountTypeSettings.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount type which will be added to the invoiced or the statistical value. `Required` `Filter(multi eq)` `Owner` |
| [EnterpriseCompany](Finance.Intrastat.DocumentAmountTypeSettings.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the setting is valid. `Required` `Filter(multi eq)` |


## Attribute Details

### AddToInvoicedValue

True= to add the amount to the invoiced value, false=otherwise. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AddToStatisticalValue

True= to add the amount to the statistical value, false=otherwise. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DocumentAmountType

The amount type which will be added to the invoiced or the statistical value. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### EnterpriseCompany

The enterprise company for which the setting is valid. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Intrastat.DocumentAmountTypeSettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Intrastat.DocumentAmountTypeSettings erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Intrastat_DocumentAmountTypeSettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Intrastat_DocumentAmountTypeSettings?$top=10>

