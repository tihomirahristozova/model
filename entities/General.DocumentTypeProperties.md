---
uid: General.DocumentTypeProperties
---
# General.DocumentTypeProperties

Default user-defined properties, which should be added to new documents. Entity: Gen_Document_Type_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentTypeProperties.md#Id) | guid |  
| [DefaultPropertyValue](General.DocumentTypeProperties.md#DefaultPropertyValue) | string (nullable) | The default value of the property when creating new documents. 
| [DefaultPropertyValueDescription](General.DocumentTypeProperties.md#DefaultPropertyValueDescription) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | Default description value of the property when creating new documents. 
| [DefaultValueId](General.DocumentTypeProperties.md#DefaultValueId) | guid (nullable) | Internal Id of the default value of the property. [Filter(multi eq)] 
| [LineNo](General.DocumentTypeProperties.md#LineNo) | int32 | Line number, unique within the document type. [Required] [Filter(ge;le)] [ORD] 
| [Required](General.DocumentTypeProperties.md#Required) | boolean | True if the property is required when creating documents of this type. [Required] [Default(false)] [Filter(eq)] 
| [RequiredFromDate](General.DocumentTypeProperties.md#RequiredFromDate) | datetime (nullable) | When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. [Filter(ge;le)] 
| [RequiredThruDate](General.DocumentTypeProperties.md#RequiredThruDate) | datetime (nullable) | When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeProperties.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The document type, for which to add user-defined properties. [Required] [Filter(multi eq)] [Owner] |
| [EnterpriseCompany](General.DocumentTypeProperties.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the current rule is valid only for the specified company. [Filter(multi eq)] |
| [Property](General.DocumentTypeProperties.md#Property) | [General.CustomProperties](General.CustomProperties.md) | The user-defined property, which should be added. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DefaultPropertyValue

> The default value of the property when creating new documents.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultPropertyValueDescription

> Default description value of the property when creating new documents.

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultValueId

> Internal Id of the default value of the property. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LineNo

> Line number, unique within the document type. [Required] [Filter(ge;le)] [ORD]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  

_Back-End Default Expression:_  
`(obj.DocumentType.DocumentTypeProperties.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.DocumentType.DocumentTypeProperties.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Required

> True if the property is required when creating documents of this type. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### RequiredFromDate

> When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequiredThruDate

> When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

> The document type, for which to add user-defined properties. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> When not null, specifies that the current rule is valid only for the specified company. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Property

> The user-defined property, which should be added. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentTypeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentTypeProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentTypeProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeProperties?$top=10>

