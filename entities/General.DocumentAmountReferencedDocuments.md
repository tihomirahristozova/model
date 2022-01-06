---
uid: General.DocumentAmountReferencedDocuments
---
# General.DocumentAmountReferencedDocuments Entity

**Namespace:** [General](General.md)  

Contains the documents which are referenced by each document amount. Entity: Gen_Document_Amount_Referenced_Documents

## Default Visualization
Default Display Text Format:  
_{DocumentAmount.Document.EntityName}_  
Default Search Members:  
_DocumentAmount.Document.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentAmounts](General.DocumentAmounts.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmountReferencedDocuments.md#id) | guid |  
| [ObjectVersion](General.DocumentAmountReferencedDocuments.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmount](General.DocumentAmountReferencedDocuments.md#documentamount) | [DocumentAmounts](General.DocumentAmounts.md) | The document amount for which the referenced document is specified. `Required` `Filter(multi eq)` `Owner` |
| [ReferencedDocument](General.DocumentAmountReferencedDocuments.md#referenceddocument) | [Documents](General.Documents.md) | The document which is referenced by the document amount. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DocumentAmount

The document amount for which the referenced document is specified. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentAmounts](General.DocumentAmounts.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ReferencedDocument

The document which is referenced by the document amount. `Required` `Filter(multi eq)`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentAmountReferencedDocuments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentAmountReferencedDocuments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountReferencedDocuments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountReferencedDocuments?$top=10>

