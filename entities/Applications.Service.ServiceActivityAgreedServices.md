---
uid: Applications.Service.ServiceActivityAgreedServices
---
# Applications.Service.ServiceActivityAgreedServices Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contains the services, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Services

## Default Visualization
Default Display Text Format:  
_{ServiceActivityService.ServiceActivity.DocumentType.Code}:{ServiceActivityService.ServiceActivity.DocumentNo}:{ServiceActivityService.LineNo} - {ServiceActivityService.ServiceActivity.DocumentType.TypeName:T}_  
Default Search Member:  
_ServiceActivityService.ServiceActivity.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Service.ServiceActivityServices](Applications.Service.ServiceActivityServices.md)  
Aggregate Root:  
[Applications.Service.ServiceActivities](Applications.Service.ServiceActivities.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AgreedQuantity](Applications.Service.ServiceActivityAgreedServices.md#agreedquantity) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity from the service agreement service line that is accounted for this service activity service line. `Unit: ServiceAgreementService.QuantityUnit` `Required` `Default(0)` `ReadOnly` 
| [Id](Applications.Service.ServiceActivityAgreedServices.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceActivityService](Applications.Service.ServiceActivityAgreedServices.md#serviceactivityservice) | [ServiceActivityServices](Applications.Service.ServiceActivityServices.md) | The `ServiceActivityService`(Applications.Service.ServiceActivity<br />AgreedServices.md#serviceactivityservice) to which this ServiceActivity<br />AgreedService belongs. `Required` `Filter(multi eq)` `ReadOnly` `Owner` |
| [ServiceAgreementService](Applications.Service.ServiceActivityAgreedServices.md#serviceagreementservice) | [ServiceAgreementServices](Applications.Service.ServiceAgreementServices.md) | Service agreement service line that records the paid or agreed in advance service or product. `Required` `Filter(multi eq)` `ReadOnly` |


## Attribute Details

### AgreedQuantity

Quantity from the service agreement service line that is accounted for this service activity service line. `Unit: ServiceAgreementService.QuantityUnit` `Required` `Default(0)` `ReadOnly`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ServiceActivityService

The `ServiceActivityService`(Applications.Service.ServiceActivityAgreedServices.md#serviceactivityservice) to which this ServiceActivityAgreedService belongs. `Required` `Filter(multi eq)` `ReadOnly` `Owner`

_Type_: **[ServiceActivityServices](Applications.Service.ServiceActivityServices.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ServiceAgreementService

Service agreement service line that records the paid or agreed in advance service or product. `Required` `Filter(multi eq)` `ReadOnly`

_Type_: **[ServiceAgreementServices](Applications.Service.ServiceAgreementServices.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceActivityAgreedServices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceActivityAgreedServices erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityAgreedServices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityAgreedServices?$top=10>

