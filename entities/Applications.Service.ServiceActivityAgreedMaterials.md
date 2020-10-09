---
uid: Applications.Service.ServiceActivityAgreedMaterials
---
# Applications.Service.ServiceActivityAgreedMaterials Entity

Contains the materials, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AgreedQuantity](Applications.Service.ServiceActivityAgreedMaterials.md#agreedquantity) | [Quantity](../data-types.md#quantity) | Quantity from the service agreement material line that is accounted for this service activity material line. [Unit: ServiceAgreementMaterial.QuantityUnit] [Required] [Default(0)] [ReadOnly] 
| [Id](Applications.Service.ServiceActivityAgreedMaterials.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#serviceactivitymaterial) | [ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md) | The [ServiceActivityMaterial](Applications.Service.ServiceActivity<br />AgreedMaterials.md#serviceactivitymaterial) to which this ServiceActivity<br />AgreedMaterial belongs. [Required] [Filter(multi eq)] [ReadOnly]  |
| [ServiceAgreementMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#serviceagreementmaterial) | [ServiceAgreementMaterials](Applications.Service.ServiceAgreementMaterials.md) | Service agreement material line that records the paid or agreed in advance material. [Required] [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### AgreedQuantity

Quantity from the service agreement material line that is accounted for this service activity material line. [Unit: ServiceAgreementMaterial.QuantityUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ServiceActivityMaterial

The [ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#serviceactivitymaterial) to which this ServiceActivityAgreedMaterial belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceAgreementMaterial

Service agreement material line that records the paid or agreed in advance material. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[ServiceAgreementMaterials](Applications.Service.ServiceAgreementMaterials.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedMaterials erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityAgreedMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityAgreedMaterials?$top=10>

