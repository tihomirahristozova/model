---
uid: Applications.Service.ServiceInvoicing
---
# Applications.Service.ServiceInvoicing Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contains invoicing ratios for the listed services. Entity: Srv_Service_Invoicing

## Default Visualization
Default Display Text Format:  
_{Service.Code}: {Service.Name:T}_  
Default Search Member:  
_Service.Code_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[Applications.Service.Services](Applications.Service.Services.md)  
Aggregate Root:  
[Applications.Service.Services](Applications.Service.Services.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceInvoicing.md#id) | guid |  
| [QuantityOfProduct](Applications.Service.ServiceInvoicing.md#quantityofproduct) | [Quantity](../data-types.md#quantity) | The quantity to invoice. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityOfService](Applications.Service.ServiceInvoicing.md#quantityofservice) | [Quantity](../data-types.md#quantity) | The quantity of service for which the invoicing is specified. [Unit: Service.MeasurementUnit] [Required] [Default(1)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Applications.Service.ServiceInvoicing.md#product) | [Products](General.Products.Products.md) | The product that should be invoiced. [Required] [Filter(multi eq)] |
| [Service](Applications.Service.ServiceInvoicing.md#service) | [Services](Applications.Service.Services.md) | The service for which the invoicing instructions are. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### QuantityOfProduct

The quantity to invoice. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityOfService

The quantity of service for which the invoicing is specified. [Unit: Service.MeasurementUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Product

The product that should be invoiced. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Service

The service for which the invoicing instructions are. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Services](Applications.Service.Services.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceInvoicing erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceInvoicing erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceInvoicing?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceInvoicing?$top=10>

