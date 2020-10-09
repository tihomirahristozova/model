---
uid: Applications.Service.ServiceAgreementLines
---
# Applications.Service.ServiceAgreementLines Entity

Service agreement lines represent the individual serviced objects that are covered by the service agreement. Entity: Srv_Service_Agreement_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceAgreementLines.md#id) | guid |  
| [LineEndDateTime](Applications.Service.ServiceAgreementLines.md#lineenddatetime) | datetime | The ending date and time of the agreement coverage for the current line. [Required] [Filter(ge;le)] 
| [LineNo](Applications.Service.ServiceAgreementLines.md#lineno) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)] 
| [LineStartDateTime](Applications.Service.ServiceAgreementLines.md#linestartdatetime) | datetime | The starting date and time of the agreement coverage for the current line. [Required] [Filter(ge;le)] 
| [Notes](Applications.Service.ServiceAgreementLines.md#notes) | string (nullable) | Notes for this ServiceAgreementLine. 
| [Quantity](Applications.Service.ServiceAgreementLines.md#quantity) | decimal | The quantity of the service object that is included in the agreement. [Required] [Default(1)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceAgreement](Applications.Service.ServiceAgreementLines.md#serviceagreement) | [ServiceAgreements](Applications.Service.ServiceAgreements.md) | The [ServiceAgreement](Applications.Service.ServiceAgreementLines.md#serviceagreement) to which this ServiceAgreementLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ServiceObject](Applications.Service.ServiceAgreementLines.md#serviceobject) | [ServiceObjects](Applications.Service.ServiceObjects.md) | The service object, which is covered by the current agreement. [Required] [Filter(multi eq)] |
| [ServiceType](Applications.Service.ServiceAgreementLines.md#servicetype) | [ServiceTypes](Applications.Service.ServiceTypes.md) | The type (level) of service that is agreed. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineEndDateTime

> The ending date and time of the agreement coverage for the current line. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### LineNo

> Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ServiceAgreement.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ServiceAgreement.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### LineStartDateTime

> The starting date and time of the agreement coverage for the current line. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

> Notes for this ServiceAgreementLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> The quantity of the service object that is included in the agreement. [Required] [Default(1)] [Filter(ge;le)]

_Type_: **decimal**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### ServiceAgreement

> The [ServiceAgreement](Applications.Service.ServiceAgreementLines.md#serviceagreement) to which this ServiceAgreementLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ServiceAgreements](Applications.Service.ServiceAgreements.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceObject

> The service object, which is covered by the current agreement. [Required] [Filter(multi eq)]

_Type_: **[ServiceObjects](Applications.Service.ServiceObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceType

> The type (level) of service that is agreed. [Required] [Filter(multi eq)]

_Type_: **[ServiceTypes](Applications.Service.ServiceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceAgreementLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceAgreementLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceAgreementLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceAgreementLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceAgreementLines?$top=10>

