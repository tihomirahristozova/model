---
uid: Applications.Service.ServiceActivityAgreedMaterials
---
# Applications.Service.ServiceActivityAgreedMaterials

Contains the materials, which were agreed for this service activity (repair), before its starting. Entity: Srv_Service_Activity_Agreed_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceActivityAgreedMaterials.md#Id) | guid |  
| [AgreedQuantity](Applications.Service.ServiceActivityAgreedMaterials.md#AgreedQuantity) | [Quantity](../data-types.md#Quantity) | Quantity from the service agreement material line that is accounted for this service activity material line. [Unit: ServiceAgreementMaterial.QuantityUnit] [Required] [Default(0)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#ServiceActivityMaterial) | [Applications.Service.ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md) | The [ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#ServiceActivityMaterial) to which this ServiceActivityAgreedMaterial belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |
| [ServiceAgreementMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#ServiceAgreementMaterial) | [Applications.Service.ServiceAgreementMaterials](Applications.Service.ServiceAgreementMaterials.md) | Service agreement material line that records the paid or agreed in advance material. [Required] [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AgreedQuantity

> Quantity from the service agreement material line that is accounted for this service activity material line. [Unit: ServiceAgreementMaterial.QuantityUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### ServiceActivityMaterial

> The [ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#ServiceActivityMaterial) to which this ServiceActivityAgreedMaterial belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[Applications.Service.ServiceActivityMaterials](Applications.Service.ServiceActivityMaterials.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceAgreementMaterial

> Service agreement material line that records the paid or agreed in advance material. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[Applications.Service.ServiceAgreementMaterials](Applications.Service.ServiceAgreementMaterials.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityAgreedMaterials erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceActivityAgreedMaterials erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityAgreedMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityAgreedMaterials?$top=10>

