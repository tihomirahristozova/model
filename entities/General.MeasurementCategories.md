---
uid: General.MeasurementCategories
---
# General.MeasurementCategories Entity

**Namespace:** [General](General.md)  

Categories of measurement units. The units within a category are directly convertable to each other. Each category contains one base unit and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Categories

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.MeasurementCategories](General.MeasurementCategories.md)  
  * [General.MeasurementUnits](General.MeasurementUnits.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.MeasurementCategories.md#id) | guid |  
| [IsDefault](General.MeasurementCategories.md#isdefault) | boolean | True=This category is the default category; false=otherwise. `Required` `Default(false)` `Filter(eq)` 
| [Name](General.MeasurementCategories.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this MeasurementCategory. `Required` `Filter(eq;like)` `ORD` 
| [ObjectVersion](General.MeasurementCategories.md#objectversion) | int32 |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| MeasurementUnits | [MeasurementUnits](General.MeasurementUnits.md) | List of `MeasurementUnit`(General.MeasurementUnits.md) child objects, based on the `General.MeasurementUnit.MeasurementCategory`(General.MeasurementUnits.md#measurementcategory) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

True=This category is the default category; false=otherwise. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this MeasurementCategory. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


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

[!list limit=1000 erp.entity=General.MeasurementCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.MeasurementCategories erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_MeasurementCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_MeasurementCategories?$top=10>

