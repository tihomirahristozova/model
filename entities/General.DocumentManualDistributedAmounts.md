---
uid: General.DocumentManualDistributedAmounts
---
# General.DocumentManualDistributedAmounts Entity

**Namespace:** [General](General.md)  

Obsolete. Not used. Entity: Gen_Document_Manual_Distributed_Amounts

## Default Visualization
Default Display Text Format:  
_{Id}: {DocumentId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentManualDistributedAmounts](General.DocumentManualDistributedAmounts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](General.DocumentManualDistributedAmounts.md#displaytext) | string |  
| [DocumentAmountTypeId](General.DocumentManualDistributedAmounts.md#documentamounttypeid) | guid | Obsolete. Not used. `Required` `Filter(multi eq)` 
| [DocumentId](General.DocumentManualDistributedAmounts.md#documentid) | guid | Obsolete. Not used. `Required` `Filter(multi eq)` 
| [DocumentLineId](General.DocumentManualDistributedAmounts.md#documentlineid) | guid | Obsolete. Not used. `Required` `Filter(multi eq)` 
| [Id](General.DocumentManualDistributedAmounts.md#id) | guid |  
| [LinePercent](General.DocumentManualDistributedAmounts.md#linepercent) | decimal (7, 6) | Obsolete. Not used. `Required` 
| [ObjectVersion](General.DocumentManualDistributedAmounts.md#objectversion) | int32 |  
| [ProductId](General.DocumentManualDistributedAmounts.md#productid) | guid | Obsolete. Not used. `Required` `Filter(multi eq)` 


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### DocumentAmountTypeId

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentId

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentLineId

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### LinePercent

Obsolete. Not used. `Required`

_Type_: **decimal (7, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ProductId

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **guid**  
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

[!list limit=1000 erp.entity=General.DocumentManualDistributedAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentManualDistributedAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentManualDistributedAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentManualDistributedAmounts?$top=10>

