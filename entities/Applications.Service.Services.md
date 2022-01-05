---
uid: Applications.Service.Services
---
# Applications.Service.Services Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contains the services, which can be performed. Entity: Srv_Services

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Service.Services](Applications.Service.Services.md)  
  * [Applications.Service.ServiceInvoicing](Applications.Service.ServiceInvoicing.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.Service.Services.md#code) | string (16) | Unique code of the service. `Required` `Filter(eq;like)` 
| [Id](Applications.Service.Services.md#id) | guid |  
| [IsActive](Applications.Service.Services.md#isactive) | boolean | Indicates wheather this service is currently used. `Required` `Default(true)` `Filter(eq)` 
| [Name](Applications.Service.Services.md#name) | string (254) | The name of the service. `Required` `Filter(eq;like)` 
| [ObjectVersion](Applications.Service.Services.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MeasurementUnit](Applications.Service.Services.md#measurementunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit in which the service rendered to the customer is quantified. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Invoicing | [ServiceInvoicing](Applications.Service.ServiceInvoicing.md) | List of `ServiceInvoicing`(Applications.Service.ServiceInvoicing.md) child objects, based on the `Applications.Service.ServiceInvoicing.Service`(Applications.Service.ServiceInvoicing.md#service) back reference 


## Attribute Details

### Code

Unique code of the service. `Required` `Filter(eq;like)`

_Type_: **string (16)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Indicates wheather this service is currently used. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of the service. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### MeasurementUnit

The measurement unit in which the service rendered to the customer is quantified. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
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

[!list limit=1000 erp.entity=Applications.Service.Services erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.Services erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_Services?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_Services?$top=10>

