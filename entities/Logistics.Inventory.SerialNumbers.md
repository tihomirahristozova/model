---
uid: Logistics.Inventory.SerialNumbers
---
# Logistics.Inventory.SerialNumbers Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Serial numbers, used by the items. Rows are created on first occurrence of the serial number in a document. Rows can be deleted after deleting the last occurence of the serial number in a document. Entity: Inv_Serial_Numbers

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.SerialNumbers.md#id) | guid |  
| [ObjectVersion](Logistics.Inventory.SerialNumbers.md#objectversion) | int32 |  
| [SerialNumberField](Logistics.Inventory.SerialNumbers.md#serialnumberfield) | string (40) | The serial number text. `Required` `Filter(multi eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Logistics.Inventory.SerialNumbers.md#product) | [Products](General.Products.Products.md) | The product, to which the serial number is bound. `Required` `Filter(multi eq)` |


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

### SerialNumberField

The serial number text. `Required` `Filter(multi eq;like)`

_Type_: **string (40)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **40**  


## Reference Details

### Product

The product, to which the serial number is bound. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
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

[!list limit=1000 erp.entity=Logistics.Inventory.SerialNumbers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.SerialNumbers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_SerialNumbers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_SerialNumbers?$top=10>

