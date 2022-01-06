---
uid: Logistics.Procurement.SupplierTypes
---
# Logistics.Procurement.SupplierTypes Entity

**Namespace:** [Logistics.Procurement](Logistics.Procurement.md)  

Supplier types are primarily used to differentiate the security level access to the different supplier groups. Entity: Scm_Supplier_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Procurement.SupplierTypes](Logistics.Procurement.SupplierTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.SupplierTypes.md#id) | guid |  
| [Name](Logistics.Procurement.SupplierTypes.md#name) | string (254) | The name of this SupplierType. `Required` `Filter(eq;like)` 
| [ObjectVersion](Logistics.Procurement.SupplierTypes.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Logistics.Procurement.SupplierTypes.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key required for accessing all suppliers of this supplier type. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this SupplierType. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### AccessKey

The access key required for accessing all suppliers of this supplier type. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
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

[!list limit=1000 erp.entity=Logistics.Procurement.SupplierTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Procurement.SupplierTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_SupplierTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_SupplierTypes?$top=10>

