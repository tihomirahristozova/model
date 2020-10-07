# General.Contacts.PartyContactMechanisms

Specifies the contact mechanisms, which are attached to the parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Party_Contact_Mechanisms

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.PartyContactMechanisms.md#Id) | guid |  
| [FromDate](General.Contacts.PartyContactMechanisms.md#FromDate) | datetime (nullable) | The first date when the contact mechanism was valid. null means unknown date. [Default(Today)] [Filter(eq;ge;le)] 
| [IsActive](General.Contacts.PartyContactMechanisms.md#IsActive) | boolean | True if the contact mechanism is currently active and can be used to contact the party. [Required] [Default(true)] [Filter(eq)] 
| [IsDefault](General.Contacts.PartyContactMechanisms.md#IsDefault) | boolean | True - when this is the default contact mechanism for this party; false - otherwise. [Required] [Default(false)] [Filter(eq)] 
| [LineOrd](General.Contacts.PartyContactMechanisms.md#LineOrd) | int32 | Consecutive number of the contact information. The number is unique within the party. [Required] 
| [NonSolicitation](General.Contacts.PartyContactMechanisms.md#NonSolicitation) | boolean | If true then Don't use the mechanism for solicitation purposes. [Required] [Default(false)] [Filter(eq)] 
| [Notes](General.Contacts.PartyContactMechanisms.md#Notes) | string (nullable) | Notes for this PartyContactMechanism. 
| [ThruDate](General.Contacts.PartyContactMechanisms.md#ThruDate) | datetime (nullable) | The last date on which the contact mechanism was valid for the party. null if the contact mechanism is still valid. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContactMechanism](General.Contacts.PartyContactMechanisms.md#ContactMechanism) | [General.Contacts.ContactMechanisms](General.Contacts.ContactMechanisms.md) | The contact mechanism of the party. [Required] [Filter(multi eq)] |
| [ContactMechanismPurpose](General.Contacts.PartyContactMechanisms.md#ContactMechanismPurpose) | [General.Contacts.ContactMechanismPurposes](General.Contacts.ContactMechanismPurposes.md) (nullable) | The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms. [Filter(multi eq)] (Introduced in version 18.2.100.0) |
| [Party](General.Contacts.PartyContactMechanisms.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party, having the contact mechanism. [Required] [Filter(multi eq)] [Owner] |
| [PersonalDataProcess](General.Contacts.PartyContactMechanisms.md#PersonalDataProcess) | [Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable) | The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown. [Filter(multi eq)] (Introduced in version 18.2.100.0) |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> The first date when the contact mechanism was valid. null means unknown date. [Default(Today)] [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### IsActive

> True if the contact mechanism is currently active and can be used to contact the party. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

> True - when this is the default contact mechanism for this party; false - otherwise. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LineOrd

> Consecutive number of the contact information. The number is unique within the party. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Party.ContactMechanisms.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Party.ContactMechanisms.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### NonSolicitation

> If true then Don't use the mechanism for solicitation purposes. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this PartyContactMechanism.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ThruDate

> The last date on which the contact mechanism was valid for the party. null if the contact mechanism is still valid. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### ContactMechanism

> The contact mechanism of the party. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.ContactMechanisms](General.Contacts.ContactMechanisms.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ContactMechanismPurpose

> The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[General.Contacts.ContactMechanismPurposes](General.Contacts.ContactMechanismPurposes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The party, having the contact mechanism. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PersonalDataProcess

> The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.PartyContactMechanisms erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyContactMechanisms erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.PartyContactMechanisms erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyContactMechanisms?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyContactMechanisms?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Party_Contact_Mechanisms?$top=10>

