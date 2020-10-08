---
uid: Applications.Service.ServiceTypes
---
# Applications.Service.ServiceTypes

Service levels. Entity: Srv_Service_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceTypes.md#Id) | guid |  
| [Description](Applications.Service.ServiceTypes.md#Description) | string (nullable) | The description of this ServiceType. 
| [IsActive](Applications.Service.ServiceTypes.md#IsActive) | boolean | True when the service type is currently active and selectable in new documents. [Required] [Default(true)] [Filter(eq)] 
| [IsDefault](Applications.Service.ServiceTypes.md#IsDefault) | boolean | True when this is the default service type for the service object type. false otherwise. [Required] [Default(false)] [Filter(eq)] 
| [Name](Applications.Service.ServiceTypes.md#Name) | string | The name of this ServiceType. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PriceList](Applications.Service.ServiceTypes.md#PriceList) | [Crm.PriceLists](Crm.PriceLists.md) (nullable) | When not null, specifies the price list that should be applied when invoicing service activities. [Filter(multi eq)] |
| [ServiceObjectType](Applications.Service.ServiceTypes.md#ServiceObjectType) | [Applications.Service.ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable) | The service object type to which this service type is applicable. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this ServiceType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsActive

> True when the service type is currently active and selectable in new documents. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

> True when this is the default service type for the service object type. false otherwise. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

> The name of this ServiceType. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### PriceList

> When not null, specifies the price list that should be applied when invoicing service activities. [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceObjectType

> The service object type to which this service type is applicable. [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceTypes?$top=10>

