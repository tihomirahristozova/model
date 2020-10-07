# Applications.Service.ServiceInvoicing

Contains invoicing ratios for the listed services. Entity: Srv_Service_Invoicing

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceInvoicing.md#Id) | guid |  
| [QuantityOfProduct](Applications.Service.ServiceInvoicing.md#QuantityOfProduct) | [Quantity](../data-types/Quantity.md) | The quantity to invoice. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityOfService](Applications.Service.ServiceInvoicing.md#QuantityOfService) | [Quantity](../data-types/Quantity.md) | The quantity of service for which the invoicing is specified. [Unit: Service.MeasurementUnit] [Required] [Default(1)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Applications.Service.ServiceInvoicing.md#Product) | [General.Products.Products](General.Products.Products.md) | The product that should be invoiced. [Required] [Filter(multi eq)] |
| [Service](Applications.Service.ServiceInvoicing.md#Service) | [Applications.Service.Services](Applications.Service.Services.md) | The service for which the invoicing instructions are. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### QuantityOfProduct

> The quantity to invoice. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityOfService

> The quantity of service for which the invoicing is specified. [Unit: Service.MeasurementUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Product

> The product that should be invoiced. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Service

> The service for which the invoicing instructions are. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Service.Services](Applications.Service.Services.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceInvoicing erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceInvoicing erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceInvoicing erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceInvoicing?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceInvoicing?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Srv_Service_Invoicing?$top=10>

