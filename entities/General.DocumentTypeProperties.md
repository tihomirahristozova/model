---
uid: General.DocumentTypeProperties
---
# General.DocumentTypeProperties Entity

Default user-defined properties, which should be added to new documents. Entity: Gen_Document_Type_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultPropertyValue](General.DocumentTypeProperties.md#defaultpropertyvalue) | string (nullable) | The default value of the property when creating new documents. 
| [DefaultProperty<br />ValueDescription](General.DocumentTypeProperties.md#defaultpropertyvaluedescription) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Default description value of the property when creating new documents. 
| [DefaultValueId](General.DocumentTypeProperties.md#defaultvalueid) | guid (nullable) | Internal Id of the default value of the property. [Filter(multi eq)] 
| [Id](General.DocumentTypeProperties.md#id) | guid |  
| [LineNo](General.DocumentTypeProperties.md#lineno) | int32 | Line number, unique within the document type. [Required] [Filter(ge;le)] [ORD] 
| [Required](General.DocumentTypeProperties.md#required) | boolean | True if the property is required when creating documents of this type. [Required] [Default(false)] [Filter(eq)] 
| [RequiredFromDate](General.DocumentTypeProperties.md#requiredfromdate) | datetime (nullable) | When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. [Filter(ge;le)] 
| [RequiredThruDate](General.DocumentTypeProperties.md#requiredthrudate) | datetime (nullable) | When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeProperties.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type, for which to add user-defined properties. [Required] [Filter(multi eq)] [Owner] |
| [EnterpriseCompany](General.DocumentTypeProperties.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the current rule is valid only for the specified company. [Filter(multi eq)] |
| [Property](General.DocumentTypeProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The user-defined property, which should be added. [Required] [Filter(multi eq)] |


## Attribute Details

### DefaultPropertyValue

The default value of the property when creating new documents.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultPropertyValueDescription

Default description value of the property when creating new documents.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultValueId

Internal Id of the default value of the property. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the document type. [Required] [Filter(ge;le)] [ORD]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  

_Back-End Default Expression:_  
`( obj.DocumentType.DocumentTypeProperties.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.DocumentType.DocumentTypeProperties.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Required

True if the property is required when creating documents of this type. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### RequiredFromDate

When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequiredThruDate

When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

The document type, for which to add user-defined properties. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

When not null, specifies that the current rule is valid only for the specified company. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The user-defined property, which should be added. [Required] [Filter(multi eq)]

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentTypeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentTypeProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeProperties?$top=10>

