---
uid: Applications.Service.ServiceAgreementLines
---
# Applications.Service.ServiceAgreementLines Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Service agreement lines represent the individual serviced objects that are covered by the service agreement. Entity: Srv_Service_Agreement_Lines

## Default Visualization
Default Display Text Format:  
_{ServiceAgreement.EntityName}_  
Default Search Members:  
_ServiceAgreement.EntityName_  
Name Data Member:  
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
| [DisplayText](Applications.Service.ServiceAgreementLines.md#displaytext) | string |  
| [Id](Applications.Service.ServiceAgreementLines.md#id) | guid |  
| [LineEndDateTime](Applications.Service.ServiceAgreementLines.md#lineenddatetime) | datetime | The ending date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)` 
| [LineNo](Applications.Service.ServiceAgreementLines.md#lineno) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` `Filter(eq)` 
| [LineStartDateTime](Applications.Service.ServiceAgreementLines.md#linestartdatetime) | datetime | The starting date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)` 
| [Notes](Applications.Service.ServiceAgreementLines.md#notes) | string (254) __nullable__ | Notes for this ServiceAgreementLine. 
| [ObjectVersion](Applications.Service.ServiceAgreementLines.md#objectversion) | int32 |  
| [Quantity](Applications.Service.ServiceAgreementLines.md#quantity) | decimal (14, 3) | The quantity of the service object that is included in the agreement. `Required` `Default(1)` `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceAgreement](Applications.Service.ServiceAgreementLines.md#serviceagreement) | [ServiceAgreements](Applications.Service.ServiceAgreements.md) | The <see cref="ServiceAgreement"/> to which this ServiceAgreementLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [ServiceObject](Applications.Service.ServiceAgreementLines.md#serviceobject) | [ServiceObjects](Applications.Service.ServiceObjects.md) | The service object, which is covered by the current agreement. `Required` `Filter(multi eq)` |
| [ServiceType](Applications.Service.ServiceAgreementLines.md#servicetype) | [ServiceTypes](Applications.Service.ServiceTypes.md) | The type (level) of service that is agreed. `Required` `Filter(multi eq)` |


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineEndDateTime

The ending date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ServiceAgreement.EndDateTime`

_Front-End Recalc Expressions:_  
`obj.ServiceAgreement.EndDateTime`
### LineNo

Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. `Required` `Filter(eq)`

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ServiceAgreement.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ServiceAgreement.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### LineStartDateTime

The starting date and time of the agreement coverage for the current line. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ServiceAgreement.StartDateTime`

_Front-End Recalc Expressions:_  
`obj.ServiceAgreement.StartDateTime`
### Notes

Notes for this ServiceAgreementLine.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Quantity

The quantity of the service object that is included in the agreement. `Required` `Default(1)` `Filter(ge;le)`

_Type_: **decimal (14, 3)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### ServiceAgreement

The <see cref="ServiceAgreement"/> to which this ServiceAgreementLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ServiceAgreements](Applications.Service.ServiceAgreements.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ServiceObject

The service object, which is covered by the current agreement. `Required` `Filter(multi eq)`

_Type_: **[ServiceObjects](Applications.Service.ServiceObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceType

The type (level) of service that is agreed. `Required` `Filter(multi eq)`

_Type_: **[ServiceTypes](Applications.Service.ServiceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceAgreementLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceAgreementLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceAgreementLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceAgreementLines?$top=10>

