---
uid: General.Resources.ResourceInstances
---
# General.Resources.ResourceInstances Entity

**Namespace:** [General.Resources](General.Resources.md)  

Represents concrete instances of resources. Entity: Gen_Resource_Instances

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Resources.Resources](General.Resources.Resources.md)  
Aggregate Root:  
[General.Resources.ResourceGroups](General.Resources.ResourceGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Resources.ResourceInstances.md#code) | string (16) | Code of the instance, unique within the resource. `Required` `Filter(eq;like)` 
| [Id](General.Resources.ResourceInstances.md#id) | guid |  
| [Name](General.Resources.ResourceInstances.md#name) | string (max) | Multilanguage resource instance name. `Required` `Filter(eq;like)` 
| [Notes](General.Resources.ResourceInstances.md#notes) | string (max) __nullable__ | Notes for this ResourceInstance. 
| [ObjectVersion](General.Resources.ResourceInstances.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](General.Resources.ResourceInstances.md#asset) | [Assets](Finance.Assets.Assets.md) (nullable) | The asset, which is represented by this resource instance. null, when the resource instance is not an asset. `Filter(multi eq)` |
| [Party](General.Resources.ResourceInstances.md#party) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which is represented by this resource instance. null, when the resource instance is not a party. `Filter(multi eq)` |
| [Resource](General.Resources.ResourceInstances.md#resource) | [Resources](General.Resources.Resources.md) | The resource of which this is instance. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Code

Code of the instance, unique within the resource. `Required` `Filter(eq;like)`

_Type_: **string (16)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage resource instance name. `Required` `Filter(eq;like)`

_Type_: **string (max)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Notes

Notes for this ResourceInstance.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Asset

The asset, which is represented by this resource instance. null, when the resource instance is not an asset. `Filter(multi eq)`

_Type_: **[Assets](Finance.Assets.Assets.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party, which is represented by this resource instance. null, when the resource instance is not a party. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

The resource of which this is instance. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Resources](General.Resources.Resources.md)**  
_Indexed_: **True**  
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

[!list limit=1000 erp.entity=General.Resources.ResourceInstances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Resources.ResourceInstances erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_ResourceInstances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_ResourceInstances?$top=10>

