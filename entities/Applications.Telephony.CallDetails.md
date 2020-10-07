# Applications.Telephony.CallDetails

Contains call detail records. Calls are phone calls, video calls and SMS messages. Entity: Cm_Call_Details

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Telephony.CallDetails.md#Id) | guid |  
| [CallType](Applications.Telephony.CallDetails.md#CallType) | [Applications.Telephony.CallDetailsRepository.CallType](Applications.Telephony.CallDetails.md#CallType) | P=Phone; V=Video; M=Message/SMS. [Required] [Default("P")] [Filter(eq)] 
| [CallUniqueId](Applications.Telephony.CallDetails.md#CallUniqueId) | string (nullable) | The unique id of the call, as reported by the telephone central. null when the central did not report unique Id. Used for integration purposes. 
| [CalledPartyNumber](Applications.Telephony.CallDetails.md#CalledPartyNumber) | string | The voice number of the party, which received the call. [Required] [Filter(eq;like)] 
| [CallingPartyNumber](Applications.Telephony.CallDetails.md#CallingPartyNumber) | string | The voice number of the originating party of the call. [Required] [Filter(eq;like)] 
| [DurationSeconds](Applications.Telephony.CallDetails.md#DurationSeconds) | int32 | The duration of the call (in seconds). [Required] [Default(0)] [Filter(ge;le)] 
| [StartTime](Applications.Telephony.CallDetails.md#StartTime) | datetime | The starting date and time of the call. [Required] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CalledParty](Applications.Telephony.CallDetails.md#CalledParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party, which received the call. null when the party was not determined successfully. [Filter(multi eq)] |
| [CallingParty](Applications.Telephony.CallDetails.md#CallingParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party, which originated the call.  null when the party was not determined successfully. [Filter(multi eq)] |
| [ExternalCompany](Applications.Telephony.CallDetails.md#ExternalCompany) | [General.Contacts.Companies](General.Contacts.Companies.md) (nullable) | The company of the external party. It can be the party itself, or the parent party, whichever is company. null when the company cannot be determined. [Filter(multi eq)] |
| [ExternalParty](Applications.Telephony.CallDetails.md#ExternalParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. null when the respective party was null, or when no external party participated in the call. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CallType

> P=Phone; V=Video; M=Message/SMS. [Required] [Default("P")] [Filter(eq)]

_Type_: **[Applications.Telephony.CallDetailsRepository.CallType](Applications.Telephony.CallDetails.md#CallType)**  
Allowed values for the [CallType](Applications.Telephony.CallDetails.md#CallType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Phone | Phone value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Phone' |
| Video | Video value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Video' |
| MessageOrSMS | MessageOrSMS value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MessageOrSMS' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Phone**  

### CallUniqueId

> The unique id of the call, as reported by the telephone central. null when the central did not report unique Id. Used for integration purposes.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CalledPartyNumber

> The voice number of the party, which received the call. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### CallingPartyNumber

> The voice number of the originating party of the call. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### DurationSeconds

> The duration of the call (in seconds). [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StartTime

> The starting date and time of the call. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### CalledParty

> The party, which received the call. null when the party was not determined successfully. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CallingParty

> The party, which originated the call.  null when the party was not determined successfully. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ExternalCompany

> The company of the external party. It can be the party itself, or the parent party, whichever is company. null when the company cannot be determined. [Filter(multi eq)]

_Type_: **[General.Contacts.Companies](General.Contacts.Companies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ExternalParty

> It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. null when the respective party was null, or when no external party participated in the call. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Telephony.CallDetails erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Telephony.CallDetails erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Telephony.CallDetails erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Telephony_CallDetails?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Telephony_CallDetails?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Call_Details?$top=10>

