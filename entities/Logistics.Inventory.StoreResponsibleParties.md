---
uid: Logistics.Inventory.StoreResponsibleParties
---
# Logistics.Inventory.StoreResponsibleParties Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Contains the list of responsible parties (usually persons) for the stores. Stores can have multiple responsible parties. Entity: Inv_Store_Responsible_Parties

## Default Visualization
Default Display Text Format:  
_{Store.Name:T}_  
Default Search Members:  
_Store.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)  
Aggregate Root:  
[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreResponsibleParties.md#id) | guid |  
| [ObjectVersion](Logistics.Inventory.StoreResponsibleParties.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ResponsibleParty](Logistics.Inventory.StoreResponsibleParties.md#responsibleparty) | [Parties](General.Contacts.Parties.md) | The responsible party (usually employee) of the store. `Required` `Filter(multi eq)` |
| [Store](Logistics.Inventory.StoreResponsibleParties.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store for which we specify the responsible party. `Required` `Filter(multi eq)` `Owner` |


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

### ResponsibleParty

The responsible party (usually employee) of the store. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The store for which we specify the responsible party. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
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

[!list limit=1000 erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreResponsibleParties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreResponsibleParties?$top=10>

