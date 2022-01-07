---
uid: Applications.Telephony.CallDetails
---
# Applications.Telephony.CallDetails Entity

**Namespace:** [Applications.Telephony](Applications.Telephony.md)  

Contains call detail records. Calls are phone calls, video calls and SMS messages. Entity: Cm_Call_Details

## Default Visualization
Default Display Text Format:  
_{CalledPartyNumber}_  
Default Search Members:  
_CalledPartyNumber_  
Code Data Member:  
_CalledPartyNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Telephony.CallDetails](Applications.Telephony.CallDetails.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CalledPartyNumber](Applications.Telephony.CallDetails.md#calledpartynumber) | string (80) | The voice number of the party, which received the call. `Required` `Filter(eq;like)` 
| [CallingPartyNumber](Applications.Telephony.CallDetails.md#callingpartynumber) | string (80) | The voice number of the originating party of the call. `Required` `Filter(eq;like)` 
| [CallType](Applications.Telephony.CallDetails.md#calltype) | [CallType](Applications.Telephony.CallDetails.md#calltype) | P=Phone; V=Video; M=Message/SMS. `Required` `Default("P")` `Filter(eq)` 
| [CallUniqueId](Applications.Telephony.CallDetails.md#calluniqueid) | string (32) __nullable__ | The unique id of the call, as reported by the telephone central. null when the central did not report unique Id. Used for integration purposes. 
| [DisplayText](Applications.Telephony.CallDetails.md#displaytext) | string |  
| [DurationSeconds](Applications.Telephony.CallDetails.md#durationseconds) | int32 | The duration of the call (in seconds). `Required` `Default(0)` `Filter(ge;le)` 
| [Id](Applications.Telephony.CallDetails.md#id) | guid |  
| [ObjectVersion](Applications.Telephony.CallDetails.md#objectversion) | int32 |  
| [StartTime](Applications.Telephony.CallDetails.md#starttime) | datetime | The starting date and time of the call. `Required` `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CalledParty](Applications.Telephony.CallDetails.md#calledparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which received the call. null when the party was not determined successfully. `Filter(multi eq)` |
| [CallingParty](Applications.Telephony.CallDetails.md#callingparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party, which originated the call.  null when the party was not determined successfully. `Filter(multi eq)` |
| [ExternalCompany](Applications.Telephony.CallDetails.md#externalcompany) | [Companies](General.Contacts.Companies.md) (nullable) | The company of the external party. It can be the party itself, or the parent party, whichever is company. null when the company cannot be determined. `Filter(multi eq)` |
| [ExternalParty](Applications.Telephony.CallDetails.md#externalparty) | [Parties](General.Contacts.Parties.md) (nullable) | It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. null when the respective party was null, or when no external party participated in the call. `Filter(multi eq)` |


## Attribute Details

### CalledPartyNumber

The voice number of the party, which received the call. `Required` `Filter(eq;like)`

_Type_: **string (80)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **80**  

### CallingPartyNumber

The voice number of the originating party of the call. `Required` `Filter(eq;like)`

_Type_: **string (80)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **80**  

### CallType

P=Phone; V=Video; M=Message/SMS. `Required` `Default("P")` `Filter(eq)`

_Type_: **[CallType](Applications.Telephony.CallDetails.md#calltype)**  
Allowed values for the `CallType`(Applications.Telephony.CallDetails.md#calltype) data attribute  
_Allowed Values (Applications.Telephony.CallDetailsRepository.CallType Enum Members)_  

| Value | Description |
| ---- | --- |
| Phone | Phone value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Phone' |
| Video | Video value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Video' |
| MessageOrSMS | MessageOrSMS value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MessageOrSMS' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Phone**  

### CallUniqueId

The unique id of the call, as reported by the telephone central. null when the central did not report unique Id. Used for integration purposes.

_Type_: **string (32) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### DurationSeconds

The duration of the call (in seconds). `Required` `Default(0)` `Filter(ge;le)`

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### StartTime

The starting date and time of the call. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### CalledParty

The party, which received the call. null when the party was not determined successfully. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CallingParty

The party, which originated the call.  null when the party was not determined successfully. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ExternalCompany

The company of the external party. It can be the party itself, or the parent party, whichever is company. null when the company cannot be determined. `Filter(multi eq)`

_Type_: **[Companies](General.Contacts.Companies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ExternalParty

It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. null when the respective party was null, or when no external party participated in the call. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
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

[!list limit=1000 erp.entity=Applications.Telephony.CallDetails erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Telephony.CallDetails erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Telephony_CallDetails?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Telephony_CallDetails?$top=10>

