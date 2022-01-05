---
uid: Applications.Service.ServiceTypes
---
# Applications.Service.ServiceTypes Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Service levels. Entity: Srv_Service_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Service.ServiceTypes](Applications.Service.ServiceTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Applications.Service.ServiceTypes.md#description) | string (max) __nullable__ | The description of this ServiceType. 
| [Id](Applications.Service.ServiceTypes.md#id) | guid |  
| [IsActive](Applications.Service.ServiceTypes.md#isactive) | boolean | True when the service type is currently active and selectable in new documents. `Required` `Default(true)` `Filter(eq)` 
| [IsDefault](Applications.Service.ServiceTypes.md#isdefault) | boolean | True when this is the default service type for the service object type. false otherwise. `Required` `Default(false)` `Filter(eq)` 
| [Name](Applications.Service.ServiceTypes.md#name) | string (254) | The name of this ServiceType. `Required` `Filter(like)` 
| [ObjectVersion](Applications.Service.ServiceTypes.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PriceList](Applications.Service.ServiceTypes.md#pricelist) | [PriceLists](Crm.PriceLists.md) (nullable) | When not null, specifies the price list that should be applied when invoicing service activities. `Filter(multi eq)` |
| [ServiceObjectType](Applications.Service.ServiceTypes.md#serviceobjecttype) | [ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable) | The service object type to which this service type is applicable. `Filter(multi eq)` |


## Attribute Details

### Description

The description of this ServiceType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True when the service type is currently active and selectable in new documents. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

True when this is the default service type for the service object type. false otherwise. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this ServiceType. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### PriceList

When not null, specifies the price list that should be applied when invoicing service activities. `Filter(multi eq)`

_Type_: **[PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceObjectType

The service object type to which this service type is applicable. `Filter(multi eq)`

_Type_: **[ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


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

[!list limit=1000 erp.entity=Applications.Service.ServiceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceTypes?$top=10>

