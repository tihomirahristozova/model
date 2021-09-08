---
uid: Applications.PersonalData.PersonalDataProcessRecipients
---
# Applications.PersonalData.PersonalDataProcessRecipients Entity

**Namespace:** [Applications.PersonalData](Applications.PersonalData.md)  

Contains recipients, to which personal data is disclosed. Entity: Pdm_Personal_Data_Process_Recipients (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{PersonalDataProcess.Name:T} #{PersonalDataProcess.Code}_  
Default Search Member:  
_PersonalDataProcess.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)  
Aggregate Root:  
[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.PersonalData.PersonalDataProcessRecipients.md#id) | guid |  
| [Notes](Applications.PersonalData.PersonalDataProcessRecipients.md#notes) | string (max) __nullable__ | Notes for this PersonalDataProcess<br />Recipient. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PersonalDataProcess](Applications.PersonalData.PersonalDataProcessRecipients.md#personaldataprocess) | [PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) | The process, whose data is disclosed to the recipient. `Required` `Filter(multi eq)` `Owner` |
| [RecipientParty](Applications.PersonalData.PersonalDataProcessRecipients.md#recipientparty) | [Parties](General.Contacts.Parties.md) | The recipient, to whom the data is disclosed. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this PersonalDataProcessRecipient.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### PersonalDataProcess

The process, whose data is disclosed to the recipient. `Required` `Filter(multi eq)` `Owner`

_Type_: **[PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### RecipientParty

The recipient, to whom the data is disclosed. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.PersonalData.PersonalDataProcessRecipients erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.PersonalData.PersonalDataProcessRecipients erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_PersonalDataProcessRecipients?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_PersonalDataProcessRecipients?$top=10>

