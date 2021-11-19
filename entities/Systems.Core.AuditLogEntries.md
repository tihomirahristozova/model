---
uid: Systems.Core.AuditLogEntries
---
# Systems.Core.AuditLogEntries Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Each record represents the occurrence of one logged event. Entity: Sys_Audit_Log_Entries (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{ApplicationName}_  
Default Search Members:  
_ApplicationName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.AuditLogEntries](Systems.Core.AuditLogEntries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ApplicationName](Systems.Core.AuditLogEntries.md#applicationname) | string (64) __nullable__ | The client application that triggered the event. Null when unknown or N/A. `Filter(eq;like)` 
| [Details](Systems.Core.AuditLogEntries.md#details) | string (max) __nullable__ | Detailed contents of the event. Contents depend on the Event Type and Event Name. 
| [EntityItemId](Systems.Core.AuditLogEntries.md#entityitemid) | guid __nullable__ | The Id of the record, which is referenced by the event. Null when unknown or N/A. `Filter(multi eq)` 
| [EntityName](Systems.Core.AuditLogEntries.md#entityname) | string (64) __nullable__ | The entity, which is being referenced by the event. Null when unknown or N/A. `Filter(eq;like)` 
| [EventClass](Systems.Core.AuditLogEntries.md#eventclass) | [EventClass](Systems.Core.AuditLogEntries.md#eventclass) | The event primary classification, which shows the source of the event. E=Entity methods; A=Auth events; S=Server events. `Required` `Filter(multi eq)` 
| [EventName](Systems.Core.AuditLogEntries.md#eventname) | string (128) __nullable__ | Specific event or method name. Contents depend on the Event Type. Null when N/A. `Filter(eq;like)` 
| [EventTimeUtc](Systems.Core.AuditLogEntries.md#eventtimeutc) | datetime | The exact date and time (in Utc) when the event occurred. `Required` `Default(Now)` `Filter(ge;le)` `ORD` 
| [EventType](Systems.Core.AuditLogEntries.md#eventtype) | [EventType](Systems.Core.AuditLogEntries.md#eventtype) | Detailed action type. EID=Read one record by Id; ELD=Load many records; EUP=Update data; EDE=Delete record; EMT=Call method; ETH=Other entity event; AIN=Login; AOU=Log out; AUP=Sign Up; AFL=Login failed; APW=Change password; ATH=Other auth event; STH=Other server event. `Required` `Filter(multi eq)` 
| [Id](Systems.Core.AuditLogEntries.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PersonalDataProcess](Systems.Core.AuditLogEntries.md#personaldataprocess) | [PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable) | The personal data process, which was used to process the data, referenced by the event. Null when unknown or N/A. `Filter(multi eq)` |
| [User](Systems.Core.AuditLogEntries.md#user) | [Users](Systems.Security.Users.md) (nullable) | The user account under which the event has occurred. Null only for events which are not user-specific. `Filter(multi eq)` |


## Attribute Details

### ApplicationName

The client application that triggered the event. Null when unknown or N/A. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Details

Detailed contents of the event. Contents depend on the Event Type and Event Name.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### EntityItemId

The Id of the record, which is referenced by the event. Null when unknown or N/A. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### EntityName

The entity, which is being referenced by the event. Null when unknown or N/A. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### EventClass

The event primary classification, which shows the source of the event. E=Entity methods; A=Auth events; S=Server events. `Required` `Filter(multi eq)`

_Type_: **[EventClass](Systems.Core.AuditLogEntries.md#eventclass)**  
Allowed values for the `EventClass`(Systems.Core.AuditLogEntries.md#eventclass) data attribute  
_Allowed Values (Systems.Core.AuditLogEntriesRepository.EventClass Enum Members)_  

| Value | Description |
| ---- | --- |
| Entity | Entity value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Entity' |
| Authentication | Authentication value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Authentication' |
| Server | Server value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Server' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EventName

Specific event or method name. Contents depend on the Event Type. Null when N/A. `Filter(eq;like)`

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### EventTimeUtc

The exact date and time (in Utc) when the event occurred. `Required` `Default(Now)` `Filter(ge;le)` `ORD`

_Type_: **datetime**  
_Indexed_: **True**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDateTime**  

### EventType

Detailed action type. EID=Read one record by Id; ELD=Load many records; EUP=Update data; EDE=Delete record; EMT=Call method; ETH=Other entity event; AIN=Login; AOU=Log out; AUP=Sign Up; AFL=Login failed; APW=Change password; ATH=Other auth event; STH=Other server event. `Required` `Filter(multi eq)`

_Type_: **[EventType](Systems.Core.AuditLogEntries.md#eventtype)**  
Allowed values for the `EventType`(Systems.Core.AuditLogEntries.md#eventtype) data attribute  
_Allowed Values (Systems.Core.AuditLogEntriesRepository.EventType Enum Members)_  

| Value | Description |
| ---- | --- |
| ReadOneRecordById | ReadOneRecordById value. Stored as 'EID'. <br /> _Database Value:_ 'EID' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ReadOneRecordById' |
| LoadManyRecords | LoadManyRecords value. Stored as 'ELD'. <br /> _Database Value:_ 'ELD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'LoadManyRecords' |
| CreateRecord | CreateRecord value. Stored as 'ECR'. <br /> _Database Value:_ 'ECR' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'CreateRecord' |
| UpdateData | UpdateData value. Stored as 'EUP'. <br /> _Database Value:_ 'EUP' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'UpdateData' |
| DeleteRecord | DeleteRecord value. Stored as 'EDE'. <br /> _Database Value:_ 'EDE' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'DeleteRecord' |
| CallMethod | CallMethod value. Stored as 'EMT'. <br /> _Database Value:_ 'EMT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CallMethod' |
| OtherEntityEvent | OtherEntityEvent value. Stored as 'ETH'. <br /> _Database Value:_ 'ETH' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'OtherEntityEvent' |
| Login | Login value. Stored as 'AIN'. <br /> _Database Value:_ 'AIN' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'Login' |
| LogOut | LogOut value. Stored as 'AOU'. <br /> _Database Value:_ 'AOU' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'LogOut' |
| SignUp | SignUp value. Stored as 'AUP'. <br /> _Database Value:_ 'AUP' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'SignUp' |
| LoginFailed | LoginFailed value. Stored as 'AFL'. <br /> _Database Value:_ 'AFL' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'LoginFailed' |
| ChangePassword | ChangePassword value. Stored as 'APW'. <br /> _Database Value:_ 'APW' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'ChangePassword' |
| OtherAuthEvent | OtherAuthEvent value. Stored as 'ATH'. <br /> _Database Value:_ 'ATH' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'OtherAuthEvent' |
| OtherServerEvent | OtherServerEvent value. Stored as 'STH'. <br /> _Database Value:_ 'STH' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'OtherServerEvent' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### PersonalDataProcess

The personal data process, which was used to process the data, referenced by the event. Null when unknown or N/A. `Filter(multi eq)`

_Type_: **[PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user account under which the event has occurred. Null only for events which are not user-specific. `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Core.AuditLogEntries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Core.AuditLogEntries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_AuditLogEntries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_AuditLogEntries?$top=10>

