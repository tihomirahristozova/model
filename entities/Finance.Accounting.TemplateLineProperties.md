---
uid: Finance.Accounting.TemplateLineProperties
---
# Finance.Accounting.TemplateLineProperties Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Contains the way to obtain the values for each required property of both the debit and the credit accounts. Entity: Acc_Template_Line_Properties

## Default Visualization
Default Display Text Format:  
_{TemplateLine.AmountColumnName}_  
Default Search Members:  
_TemplateLine.AmountColumnName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Accounting.TemplateLines](Finance.Accounting.TemplateLines.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConstantValueId](Finance.Accounting.TemplateLineProperties.md#constantvalueid) | guid __nullable__ | The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant. `Filter(multi eq)` 
| [Id](Finance.Accounting.TemplateLineProperties.md#id) | guid |  
| [IsDebit](Finance.Accounting.TemplateLineProperties.md#isdebit) | boolean | If Is_Debit=true then this property is for the debit account in the template line for which is this record. If Is_Debit=false then the property is for the credit account. `Required` `Default(true)` `Filter(eq)` 
| [PropertyDescription](Finance.Accounting.TemplateLineProperties.md#propertydescription) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant). 
| [PropertyNo](Finance.Accounting.TemplateLineProperties.md#propertyno) | int32 | The ordinal position of the property value in the item key of the account. `Required` `Filter(eq)` 
| [PropertyValueSource](Finance.Accounting.TemplateLineProperties.md#propertyvaluesource) | string (2000) | Source for the property value according to the chosen source type. `Required` 
| [PropertyValueSourceType](Finance.Accounting.TemplateLineProperties.md#propertyvaluesourcetype) | string (64) | Type of source for the property value. For example: System properties, User properties for document, Constant, ... `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](Finance.Accounting.TemplateLineProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The property which value will be included in the item key of the account. `Required` `Filter(multi eq)` |
| [TemplateLine](Finance.Accounting.TemplateLineProperties.md#templateline) | [TemplateLines](Finance.Accounting.TemplateLines.md) | The `TemplateLine`(Finance.Accounting.TemplateLineProperties.md#templateline) to which this TemplateLineProperty belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ConstantValueId

The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDebit

If Is_Debit=true then this property is for the debit account in the template line for which is this record. If Is_Debit=false then the property is for the credit account. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PropertyDescription

Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant).

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyNo

The ordinal position of the property value in the item key of the account. `Required` `Filter(eq)`

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PropertyValueSource

Source for the property value according to the chosen source type. `Required`

_Type_: **string (2000)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2000**  

### PropertyValueSourceType

Type of source for the property value. For example: System properties, User properties for document, Constant, ... `Required`

_Type_: **string (64)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### Property

The property which value will be included in the item key of the account. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TemplateLine

The `TemplateLine`(Finance.Accounting.TemplateLineProperties.md#templateline) to which this TemplateLineProperty belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[TemplateLines](Finance.Accounting.TemplateLines.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.TemplateLineProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.TemplateLineProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_TemplateLineProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_TemplateLineProperties?$top=10>

