---
uid: Applications.PersonalData.DataSubjectRightRequests
---
# Applications.PersonalData.DataSubjectRightRequests Entity

**Namespace:** [Applications.PersonalData](Applications.PersonalData.md)  

Contains user requests for application of user rights. Entity: Pdm_Data_Subject_Right_Requests (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{Id}: {EnterpriseCompanyId}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.PersonalData.DataSubjectRightRequests](Applications.PersonalData.DataSubjectRightRequests.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompletedOnUtc](Applications.PersonalData.DataSubjectRightRequests.md#completedonutc) | datetime __nullable__ | Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented. 
| [CreatedOnUtc](Applications.PersonalData.DataSubjectRightRequests.md#createdonutc) | datetime | The date and time (in UTC), when the request was created. `Required` `Default(Now)` 
| [Id](Applications.PersonalData.DataSubjectRightRequests.md#id) | guid |  
| [Notes](Applications.PersonalData.DataSubjectRightRequests.md#notes) | string (max) __nullable__ | This should usually contain detailed implementation notes. 
| [RequestedRight](Applications.PersonalData.DataSubjectRightRequests.md#requestedright) | [RequestedRight](Applications.PersonalData.DataSubjectRightRequests.md#requestedright) | The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other. `Required` `Filter(eq)` 
| [Status](Applications.PersonalData.DataSubjectRightRequests.md#status) | [Status](Applications.PersonalData.DataSubjectRightRequests.md#status) | The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompletedByUser](Applications.PersonalData.DataSubjectRightRequests.md#completedbyuser) | [Users](Systems.Security.Users.md) (nullable) | The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown. `Filter(multi eq)` `ReadOnly` |
| [CreatedByUser](Applications.PersonalData.DataSubjectRightRequests.md#createdbyuser) | [Users](Systems.Security.Users.md) (nullable) | The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person. `Filter(multi eq)` `ReadOnly` |
| [EnterpriseCompany](Applications.PersonalData.DataSubjectRightRequests.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company, to which the request was made. `Required` `Filter(multi eq)` |
| [Person](Applications.PersonalData.DataSubjectRightRequests.md#person) | [Persons](General.Contacts.Persons.md) | The person, whose data will be corrected with the request. . `Required` `Filter(multi eq)` |


## Attribute Details

### CompletedOnUtc

Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CreatedOnUtc

The date and time (in UTC), when the request was created. `Required` `Default(Now)`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

This should usually contain detailed implementation notes.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RequestedRight

The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other. `Required` `Filter(eq)`

_Type_: **[RequestedRight](Applications.PersonalData.DataSubjectRightRequests.md#requestedright)**  
Allowed values for the `RequestedRight`(Applications.PersonalData.DataSubjectRightRequests.md#requestedright) data attribute  
_Allowed Values (Applications.PersonalData.DataSubjectRightRequestsRepository.RequestedRight Enum Members)_  

| Value | Description |
| ---- | --- |
| Rectify | Rectify value. Stored as 'REC'. <br /> _Database Value:_ 'REC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Rectify' |
| Erasure | Erasure value. Stored as 'ERA'. <br /> _Database Value:_ 'ERA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Erasure' |
| Restrict | Restrict value. Stored as 'RES'. <br /> _Database Value:_ 'RES' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Restrict' |
| Portability | Portability value. Stored as 'POR'. <br /> _Database Value:_ 'POR' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Portability' |
| Object | Object value. Stored as 'OBJ'. <br /> _Database Value:_ 'OBJ' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Object' |
| Other | Other value. Stored as 'OTH'. <br /> _Database Value:_ 'OTH' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Status

The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied. `Required`

_Type_: **[Status](Applications.PersonalData.DataSubjectRightRequests.md#status)**  
Allowed values for the `Status`(Applications.PersonalData.DataSubjectRightRequests.md#status) data attribute  
_Allowed Values (Applications.PersonalData.DataSubjectRightRequestsRepository.Status Enum Members)_  

| Value | Description |
| ---- | --- |
| Requested | Requested value. Stored as '1'. <br /> _Database Value:_ '1' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Requested' |
| Reviewing | Reviewing value. Stored as '2'. <br /> _Database Value:_ '2' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Reviewing' |
| Executing | Executing value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Executing' |
| Implemented | Implemented value. Stored as '4'. <br /> _Database Value:_ '4' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Implemented' |
| Denied | Denied value. Stored as '5'. <br /> _Database Value:_ '5' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Denied' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CompletedByUser

The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown. `Filter(multi eq)` `ReadOnly`

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CreatedByUser

The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person. `Filter(multi eq)` `ReadOnly`

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The enterprise company, to which the request was made. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

The person, whose data will be corrected with the request. . `Required` `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.PersonalData.DataSubjectRightRequests erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.PersonalData.DataSubjectRightRequests erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_DataSubjectRightRequests?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_DataSubjectRightRequests?$top=10>

