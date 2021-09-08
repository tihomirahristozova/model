---
uid: Applications.Service.ServiceObjects
---
# Applications.Service.ServiceObjects Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contains the serviceable objects. The service objects can be covered by service agreements, serviced in service activities, etc. Entity: Srv_Service_Objects

## Default Visualization
Default Display Text Format:  
_{Name:T} #{SerialNumber}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceObjects.md#id) | guid |  
| [Name](Applications.Service.ServiceObjects.md#name) | string (254) | The name of this ServiceObject. `Required` `Filter(eq;like)` 
| [Notes](Applications.Service.ServiceObjects.md#notes) | string (254) __nullable__ | Notes for this ServiceObject. 
| [SerialNumber](Applications.Service.ServiceObjects.md#serialnumber) | string (32) __nullable__ | The serial number of the item, that is being serviced. `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Service.ServiceObjects.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this ServiceObject applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [Product](Applications.Service.ServiceObjects.md#product) | [Products](General.Products.Products.md) (nullable) | When not-null identifies the product, from which the service object was created. `Filter(multi eq)` |
| [SerialNumberObj](Applications.Service.ServiceObjects.md#serialnumberobj) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Serial number for the product, that corresponds to this service object. If there is no product, then the other field for 'Serial number' is used to specify this data. `Filter(multi eq)` |
| [ServicedProduct](Applications.Service.ServiceObjects.md#servicedproduct) | [Products](General.Products.Products.md) (nullable) | The product, which is used to physically store the service object, when it is serviced. Need to be specified, only when it is different from Product; otherwise, it is null. `Filter(multi eq)` |
| [ServiceObjectType](Applications.Service.ServiceObjects.md#serviceobjecttype) | [ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable) | When not null specifies the type of the service object. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ServiceObject. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Notes

Notes for this ServiceObject.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### SerialNumber

The serial number of the item, that is being serviced. `Filter(like)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.SerialNumberObj != null), null, obj.SerialNumber)`

## Reference Details

### EnterpriseCompany

The Enterprise Company to which this ServiceObject applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

When not-null identifies the product, from which the service object was created. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumberObj

Serial number for the product, that corresponds to this service object. If there is no product, then the other field for 'Serial number' is used to specify this data. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.SerialNumber != null), null, obj.SerialNumberObj)`
### ServicedProduct

The product, which is used to physically store the service object, when it is serviced. Need to be specified, only when it is different from Product; otherwise, it is null. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceObjectType

When not null specifies the type of the service object. `Filter(multi eq)`

_Type_: **[ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceObjects erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceObjects erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceObjects?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceObjects?$top=10>

