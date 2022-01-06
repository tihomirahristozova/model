---
uid: Crm.PriceTypes
---
# Crm.PriceTypes Entity

**Namespace:** [Crm](Crm.md)  

Price types. Entity: Crm_Price_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.PriceTypes](Crm.PriceTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.PriceTypes.md#code) | string (16) | Short identification code of the price type. `Required` `Filter(eq)` `ORD` 
| [Id](Crm.PriceTypes.md#id) | guid |  
| [Name](Crm.PriceTypes.md#name) | string (254) | Full name of the price type. `Required` `Filter(eq;like)` 
| [Notes](Crm.PriceTypes.md#notes) | string (max) __nullable__ | Notes for this PriceType. 
| [ObjectVersion](Crm.PriceTypes.md#objectversion) | int32 |  
| [OrdinalPos](Crm.PriceTypes.md#ordinalpos) | int32 | Priority position of the price type, with respect to the other price types. `Required` `ORD` 


## Attribute Details

### Code

Short identification code of the price type. `Required` `Filter(eq)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Full name of the price type. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this PriceType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### OrdinalPos

Priority position of the price type, with respect to the other price types. `Required` `ORD`

_Type_: **int32**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  


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

[!list limit=1000 erp.entity=Crm.PriceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.PriceTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PriceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PriceTypes?$top=10>

