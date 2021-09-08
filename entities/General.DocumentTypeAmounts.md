---
uid: General.DocumentTypeAmounts
---
# General.DocumentTypeAmounts Entity

**Namespace:** [General](General.md)  

Specifies amount types, that should be automatically added to documents of a given type. Entity: Gen_Document_Type_Amounts

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
| [DefaultPercent](General.DocumentTypeAmounts.md#defaultpercent) | decimal (7, 6) __nullable__ | Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type. 
| [Id](General.DocumentTypeAmounts.md#id) | guid |  
| [RequiredFromDate](General.DocumentTypeAmounts.md#requiredfromdate) | date __nullable__ | When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)` 
| [RequiredThruDate](General.DocumentTypeAmounts.md#requiredthrudate) | date __nullable__ | When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date. `Filter(ge;le)` 
| [UserCanChangeInput](General.DocumentTypeAmounts.md#usercanchangeinput) | boolean | True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](General.DocumentTypeAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount type that should be automatically added to the documents of the specified type. `Required` `Filter(multi eq)` |
| [DocumentType](General.DocumentTypeAmounts.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the amount type is specified. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DefaultPercent

Default input percent. Valid only for amount types, supporting percent and takes precedence over Default_Percent in the definition of the amount type.

_Type_: **decimal (7, 6) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### RequiredFromDate

When not null, specifies a date, after which the amount becomes required for the current document type. The date is compared against the document date. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### RequiredThruDate

When not null, specifies a date, up to which the amount is required for the current document type. The date is compared against the document date. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UserCanChangeInput

True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### DocumentAmountType

The amount type that should be automatically added to the documents of the specified type. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the amount type is specified. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeAmounts?$top=10>

