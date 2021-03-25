---
uid: General.Contacts.PartyContactMechanisms
---
# General.Contacts.PartyContactMechanisms Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Specifies the contact mechanisms, which are attached to the parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Party_Contact_Mechanisms

## Default Visualization
Default Display Text Format:  
_{Party.PartyCode}: {Party.PartyName:T}_  
Default Search Member:  
_Party.PartyCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Parties](General.Contacts.Parties.md)  
Aggregate Root:  
[General.Contacts.Parties](General.Contacts.Parties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](General.Contacts.PartyContactMechanisms.md#fromdate) | datetime __nullable__ | The first date when the contact mechanism was valid. null means unknown date. `Default(Today)` `Filter(eq;ge;le)` 
| [Id](General.Contacts.PartyContactMechanisms.md#id) | guid |  
| [IsActive](General.Contacts.PartyContactMechanisms.md#isactive) | boolean | True if the contact mechanism is currently active and can be used to contact the party. `Required` `Default(true)` `Filter(eq)` 
| [IsDefault](General.Contacts.PartyContactMechanisms.md#isdefault) | boolean | True - when this is the default contact mechanism for this party; false - otherwise. `Required` `Default(false)` `Filter(eq)` 
| [LineOrd](General.Contacts.PartyContactMechanisms.md#lineord) | int32 | Consecutive number of the contact information. The number is unique within the party. `Required` 
| [NonSolicitation](General.Contacts.PartyContactMechanisms.md#nonsolicitation) | boolean | If true then Don't use the mechanism for solicitation purposes. `Required` `Default(false)` `Filter(eq)` 
| [Notes](General.Contacts.PartyContactMechanisms.md#notes) | string (254) __nullable__ | Notes for this PartyContactMechanism. 
| [ThruDate](General.Contacts.PartyContactMechanisms.md#thrudate) | datetime __nullable__ | The last date on which the contact mechanism was valid for the party. null if the contact mechanism is still valid. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContactMechanism](General.Contacts.PartyContactMechanisms.md#contactmechanism) | [ContactMechanisms](General.Contacts.ContactMechanisms.md) | The contact mechanism of the party. `Required` `Filter(multi eq)` |
| [ContactMechanismPurpose](General.Contacts.PartyContactMechanisms.md#contactmechanismpurpose) | [ContactMechanismPurposes](General.Contacts.ContactMechanismPurposes.md) (nullable) | The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms. `Filter(multi eq)` `Introduced in version 18.2` |
| [Party](General.Contacts.PartyContactMechanisms.md#party) | [Parties](General.Contacts.Parties.md) | The party, having the contact mechanism. `Required` `Filter(multi eq)` `Owner` |
| [PersonalDataProcess](General.Contacts.PartyContactMechanisms.md#personaldataprocess) | [PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable) | The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown. `Filter(multi eq)` `Introduced in version 18.2` |


## Attribute Details

### FromDate

The first date when the contact mechanism was valid. null means unknown date. `Default(Today)` `Filter(eq;ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the contact mechanism is currently active and can be used to contact the party. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

True - when this is the default contact mechanism for this party; false - otherwise. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LineOrd

Consecutive number of the contact information. The number is unique within the party. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Party.ContactMechanisms.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Party.ContactMechanisms.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### NonSolicitation

If true then Don't use the mechanism for solicitation purposes. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this PartyContactMechanism.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ThruDate

The last date on which the contact mechanism was valid for the party. null if the contact mechanism is still valid. `Filter(eq;ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### ContactMechanism

The contact mechanism of the party. `Required` `Filter(multi eq)`

_Type_: **[ContactMechanisms](General.Contacts.ContactMechanisms.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ContactMechanismPurpose

The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms. `Filter(multi eq)` `Introduced in version 18.2`

_Type_: **[ContactMechanismPurposes](General.Contacts.ContactMechanismPurposes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party, having the contact mechanism. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PersonalDataProcess

The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown. `Filter(multi eq)` `Introduced in version 18.2`

_Type_: **[PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.PartyContactMechanisms erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyContactMechanisms erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyContactMechanisms?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyContactMechanisms?$top=10>

