# Applications.Service.ServiceActivityAgreedServices

Contains the services, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Services

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceActivityAgreedServices.md#Id) | guid |  
| [AgreedQuantity](Applications.Service.ServiceActivityAgreedServices.md#AgreedQuantity) | [Quantity](../data-types/Quantity.md) | Quantity from the service agreement service line that is accounted for this service activity service line. [Unit: ServiceAgreementService.QuantityUnit] [Required] [Default(0)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceActivityService](Applications.Service.ServiceActivityAgreedServices.md#ServiceActivityService) | [Applications.Service.ServiceActivityServices](Applications.Service.ServiceActivityServices.md) | The [ServiceActivityService](Applications.Service.ServiceActivityAgreedServices.md#ServiceActivityService) to which this ServiceActivityAgreedService belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |
| [ServiceAgreementService](Applications.Service.ServiceActivityAgreedServices.md#ServiceAgreementService) | [Applications.Service.ServiceAgreementServices](Applications.Service.ServiceAgreementServices.md) | Service agreement service line that records the paid or agreed in advance service or product. [Required] [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AgreedQuantity

> Quantity from the service agreement service line that is accounted for this service activity service line. [Unit: ServiceAgreementService.QuantityUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### ServiceActivityService

> The [ServiceActivityService](Applications.Service.ServiceActivityAgreedServices.md#ServiceActivityService) to which this ServiceActivityAgreedService belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[Applications.Service.ServiceActivityServices](Applications.Service.ServiceActivityServices.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceAgreementService

> Service agreement service line that records the paid or agreed in advance service or product. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[Applications.Service.ServiceAgreementServices](Applications.Service.ServiceAgreementServices.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedServices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedServices erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceActivityAgreedServices erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityAgreedServices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityAgreedServices?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Srv_Service_Activity_Agreed_Services?$top=10>

