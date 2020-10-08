---
uid: Finance.Accounting.TemplateLineProperties
---
# Finance.Accounting.TemplateLineProperties

Contains the way to obtain the values for each required property of both the debit and the credit accounts. Entity: Acc_Template_Line_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConstantValueId](Finance.Accounting.TemplateLineProperties.md#constantvalueid) | guid (nullable) | The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant. [Filter(multi eq)] 
| [Id](Finance.Accounting.TemplateLineProperties.md#id) | guid |  
| [IsDebit](Finance.Accounting.TemplateLineProperties.md#isdebit) | boolean | If Is_Debit=true then this property is for the debit account in the template line for which is this record. If Is_Debit=false then the property is for the credit account. [Required] [Default(true)] [Filter(eq)] 
| [PropertyDescription](Finance.Accounting.TemplateLineProperties.md#propertydescription) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant). 
| [PropertyNo](Finance.Accounting.TemplateLineProperties.md#propertyno) | int32 | The ordinal position of the property value in the item key of the account. [Required] [Filter(eq)] 
| [PropertyValueSource](Finance.Accounting.TemplateLineProperties.md#propertyvaluesource) | string | Source for the property value according to the chosen source type. [Required] 
| [PropertyValueSourceType](Finance.Accounting.TemplateLineProperties.md#propertyvaluesourcetype) | string | Type of source for the property value. For example: System properties, User properties for document, Constant, ... [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](Finance.Accounting.TemplateLineProperties.md#property) | [General.CustomProperties](General.CustomProperties.md) | The property which value will be included in the item key of the account. [Required] [Filter(multi eq)] |
| [TemplateLine](Finance.Accounting.TemplateLineProperties.md#templateline) | [Finance.Accounting.TemplateLines](Finance.Accounting.TemplateLines.md) | The [TemplateLine](Finance.Accounting.TemplateLineProperties.md#templateline) to which this TemplateLineProperty belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### ConstantValueId

> The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDebit

> If Is_Debit=true then this property is for the debit account in the template line for which is this record. If Is_Debit=false then the property is for the credit account. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PropertyDescription

> Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant).

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyNo

> The ordinal position of the property value in the item key of the account. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PropertyValueSource

> Source for the property value according to the chosen source type. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyValueSourceType

> Type of source for the property value. For example: System properties, User properties for document, Constant, ... [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Property

> The property which value will be included in the item key of the account. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TemplateLine

> The [TemplateLine](Finance.Accounting.TemplateLineProperties.md#templateline) to which this TemplateLineProperty belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Accounting.TemplateLines](Finance.Accounting.TemplateLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.TemplateLineProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.TemplateLineProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.TemplateLineProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_TemplateLineProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_TemplateLineProperties?$top=10>

