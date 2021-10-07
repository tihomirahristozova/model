---
uid: Applications.Service.ServiceTypes
---
# Applications.Service.ServiceTypes Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Service levels. Entity: Srv_Service_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

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


## Reference Details

### PriceList

When not null, specifies the price list that should be applied when invoicing service activities. `Filter(multi eq)`

_Type_: **[PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceObjectType

The service object type to which this service type is applicable. `Filter(multi eq)`

_Type_: **[ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceTypes?$top=10>

