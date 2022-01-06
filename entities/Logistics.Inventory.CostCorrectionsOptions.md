---
uid: Logistics.Inventory.CostCorrectionsOptions
---
# Logistics.Inventory.CostCorrectionsOptions Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Options per document type for the cost corrections. Entity: Inv_Cost_Corrections_Options

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Inventory.CostCorrectionsOptions](Logistics.Inventory.CostCorrectionsOptions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.CostCorrectionsOptions.md#id) | guid |  
| [ObjectVersion](Logistics.Inventory.CostCorrectionsOptions.md#objectversion) | int32 |  
| [ResetTransactions<br />StateOnReleasing](Logistics.Inventory.CostCorrectionsOptions.md#resettransactionsstateonreleasing) | boolean | When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents. `Required` `Default(false)` `Filter(eq)` 
| [ScheduleDocumentEvents](Logistics.Inventory.CostCorrectionsOptions.md#scheduledocumentevents) | boolean | Indicates wheather the document events caused by the cost correction should be scheduled for later procession. `Required` `Default(false)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](Logistics.Inventory.CostCorrectionsOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which we specify the options. `Required` `Filter(multi eq)` |


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

### ResetTransactionsStateOnReleasing

When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ScheduleDocumentEvents

Indicates wheather the document events caused by the cost correction should be scheduled for later procession. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DocumentType

The document type for which we specify the options. `Required` `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
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

[!list limit=1000 erp.entity=Logistics.Inventory.CostCorrectionsOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.CostCorrectionsOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_CostCorrectionsOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_CostCorrectionsOptions?$top=10>

