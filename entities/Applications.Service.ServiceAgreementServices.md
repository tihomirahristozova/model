---
uid: Applications.Service.ServiceAgreementServices
---
# Applications.Service.ServiceAgreementServices Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contains the free services, included in the service agreement. Entity: Srv_Service_Agreement_Services

## Default Visualization
Default Display Text Format:  
_{ServiceAgreement.EntityName}_  
Default Search Members:  
_ServiceAgreement.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Service.ServiceAgreements](Applications.Service.ServiceAgreements.md)  
Aggregate Root:  
[Applications.Service.ServiceAgreements](Applications.Service.ServiceAgreements.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndDate](Applications.Service.ServiceAgreementServices.md#enddate) | datetime __nullable__ | End date to which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities. 
| [Id](Applications.Service.ServiceAgreementServices.md#id) | guid |  
| [LineNo](Applications.Service.ServiceAgreementServices.md#lineno) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` 
| [Quantity](Applications.Service.ServiceAgreementServices.md#quantity) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity of the agreed servcice or product. `Unit: QuantityUnit` `Required` 
| [StartDate](Applications.Service.ServiceAgreementServices.md#startdate) | datetime __nullable__ | Start date from which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [QuantityUnit](Applications.Service.ServiceAgreementServices.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |
| [Service](Applications.Service.ServiceAgreementServices.md#service) | [Services](Applications.Service.Services.md) (nullable) | Paid or agreed in advance service that won't be invoiced after service activities (if Service_Id is filled then Service_Product_Id must be null). `Filter(multi eq)` |
| [ServiceAgreement](Applications.Service.ServiceAgreementServices.md#serviceagreement) | [ServiceAgreements](Applications.Service.ServiceAgreements.md) | The `ServiceAgreement`(Applications.Service.ServiceAgreementServices.md#serviceagreement) to which this ServiceAgreementService belongs. `Required` `Filter(multi eq)` `Owner` |
| [ServiceProduct](Applications.Service.ServiceAgreementServices.md#serviceproduct) | [Products](General.Products.Products.md) (nullable) | Paid or agreed in advance product that will be substracted from the invoiced products from service activities (if Service_Product_Id is filled then Service_Id must be null). `Filter(multi eq)` |


## Attribute Details

### EndDate

End date to which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ServiceAgreement.Services.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ServiceAgreement.Services.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Quantity

Quantity of the agreed servcice or product. `Unit: QuantityUnit` `Required`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartDate

Start date from which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Service.MeasurementUnit.IfNullThen( obj.ServiceProduct.MeasurementUnit).IfNullThen( obj.QuantityUnit)`
### Service

Paid or agreed in advance service that won't be invoiced after service activities (if Service_Id is filled then Service_Product_Id must be null). `Filter(multi eq)`

_Type_: **[Services](Applications.Service.Services.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.ServiceProduct != null), null, obj.Service)`
### ServiceAgreement

The `ServiceAgreement`(Applications.Service.ServiceAgreementServices.md#serviceagreement) to which this ServiceAgreementService belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ServiceAgreements](Applications.Service.ServiceAgreements.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ServiceProduct

Paid or agreed in advance product that will be substracted from the invoiced products from service activities (if Service_Product_Id is filled then Service_Id must be null). `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.Service != null), null, obj.ServiceProduct)`


## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceAgreementServices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceAgreementServices erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceAgreementServices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceAgreementServices?$top=10>

