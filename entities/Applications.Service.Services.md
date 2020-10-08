---
uid: Applications.Service.Services
---
# Applications.Service.Services

Contains the services, which can be performed. Entity: Srv_Services

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.Services.md#Id) | guid |  
| [IsActive](Applications.Service.Services.md#IsActive) | boolean | Indicates wheather this service is currently used. [Required] [Default(true)] [Filter(eq)] 
| [Code](Applications.Service.Services.md#Code) | string | Unique code of the service. [Required] [Filter(eq;like)] 
| [Name](Applications.Service.Services.md#Name) | string | The name of the service. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MeasurementUnit](Applications.Service.Services.md#MeasurementUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit in which the service rendered to the customer is quantified. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Invoicing | [Applications.Service.ServiceInvoicing](Applications.Service.ServiceInvoicing.md) | List of [ServiceInvoicing](Applications.Service.ServiceInvoicing.md) child objects, based on the [Applications.Service.ServiceInvoicing.Service](Applications.Service.ServiceInvoicing.md#Service) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates wheather this service is currently used. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Code

> Unique code of the service. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> The name of the service. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### MeasurementUnit

> The measurement unit in which the service rendered to the customer is quantified. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.Services erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.Services erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.Services erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_Services?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_Services?$top=10>

