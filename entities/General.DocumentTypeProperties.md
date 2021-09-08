---
uid: General.DocumentTypeProperties
---
# General.DocumentTypeProperties Entity

**Namespace:** [General](General.md)  

Default user-defined properties, which should be added to new documents. Entity: Gen_Document_Type_Properties

## Default Visualization
Default Display Text Format:  
_{DocumentType.EntityName:T} #{DocumentType.Code}_  
Default Search Member:  
_DocumentType.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentTypes](General.DocumentTypes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultPropertyValue](General.DocumentTypeProperties.md#defaultpropertyvalue) | string (254) __nullable__ | The default value of the property when creating new documents. 
| [DefaultProperty<br />ValueDescription](General.DocumentTypeProperties.md#defaultpropertyvaluedescription) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | Default description value of the property when creating new documents. 
| [DefaultValueId](General.DocumentTypeProperties.md#defaultvalueid) | guid __nullable__ | Internal Id of the default value of the property. `Filter(multi eq)` 
| [Id](General.DocumentTypeProperties.md#id) | guid |  
| [LineNo](General.DocumentTypeProperties.md#lineno) | int32 | Line number, unique within the document type. `Required` `Filter(ge;le)` `ORD` 
| [Required](General.DocumentTypeProperties.md#required) | boolean | True if the property is required when creating documents of this type. `Required` `Default(false)` `Filter(eq)` 
| [RequiredFromDate](General.DocumentTypeProperties.md#requiredfromdate) | datetime __nullable__ | When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)` 
| [RequiredThruDate](General.DocumentTypeProperties.md#requiredthrudate) | datetime __nullable__ | When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeProperties.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type, for which to add user-defined properties. `Required` `Filter(multi eq)` `Owner` |
| [EnterpriseCompany](General.DocumentTypeProperties.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the current rule is valid only for the specified company. `Filter(multi eq)` |
| [Property](General.DocumentTypeProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The user-defined property, which should be added. `Required` `Filter(multi eq)` |


## Attribute Details

### DefaultPropertyValue

The default value of the property when creating new documents.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### DefaultPropertyValueDescription

Default description value of the property when creating new documents.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultValueId

Internal Id of the default value of the property. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the document type. `Required` `Filter(ge;le)` `ORD`

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  

_Back-End Default Expression:_  
`( obj.DocumentType.DocumentTypeProperties.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.DocumentType.DocumentTypeProperties.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Required

True if the property is required when creating documents of this type. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### RequiredFromDate

When not null, specifies a date, after which the property becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequiredThruDate

When not null, specifies a date, up to which the property is required for the current document type. The date is compared against the document date. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### DocumentType

The document type, for which to add user-defined properties. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### EnterpriseCompany

When not null, specifies that the current rule is valid only for the specified company. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The user-defined property, which should be added. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeProperties?$top=10>

