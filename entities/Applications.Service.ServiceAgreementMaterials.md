---
uid: Applications.Service.ServiceAgreementMaterials
---
# Applications.Service.ServiceAgreementMaterials Entity

Contains the free materials, included in the service agreement. Entity: Srv_Service_Agreement_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndDate](Applications.Service.ServiceAgreementMaterials.md#enddate) | datetime (nullable) | End date to which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities. 
| [Id](Applications.Service.ServiceAgreementMaterials.md#id) | guid |  
| [LineNo](Applications.Service.ServiceAgreementMaterials.md#lineno) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] 
| [Quantity](Applications.Service.ServiceAgreementMaterials.md#quantity) | [Quantity](../data-types.md#quantity) | Quantity of the agreed material. [Unit: QuantityUnit] [Required] 
| [QuantityBase](Applications.Service.ServiceAgreementMaterials.md#quantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [StandardQuantityBase](Applications.Service.ServiceAgreementMaterials.md#standardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2] 
| [StartDate](Applications.Service.ServiceAgreementMaterials.md#startdate) | datetime (nullable) | Start date from which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Applications.Service.ServiceAgreementMaterials.md#product) | [Products](General.Products.Products.md) | Paid or agreed in advance material that won't be invoiced after service activities. [Required] [Filter(multi eq)] |
| [QuantityUnit](Applications.Service.ServiceAgreementMaterials.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [ServiceAgreement](Applications.Service.ServiceAgreementMaterials.md#serviceagreement) | [ServiceAgreements](Applications.Service.ServiceAgreements.md) | The [ServiceAgreement](Applications.Service.ServiceAgreementMaterials.md#serviceagreement) to which this ServiceAgreementMaterial belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### EndDate

End date to which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ServiceAgreement.Materials.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ServiceAgreement.Materials.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Quantity

Quantity of the agreed material. [Unit: QuantityUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### QuantityBase

The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StartDate

Start date from which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Product

Paid or agreed in advance material that won't be invoiced after service activities. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceAgreement

The [ServiceAgreement](Applications.Service.ServiceAgreementMaterials.md#serviceagreement) to which this ServiceAgreementMaterial belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ServiceAgreements](Applications.Service.ServiceAgreements.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceAgreementMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceAgreementMaterials erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceAgreementMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceAgreementMaterials?$top=10>

