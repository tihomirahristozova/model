---
uid: Crm.Presales.LeadUserStages
---
# Crm.Presales.LeadUserStages Entity

**Namespace:** [Crm.Presales](Crm.Presales.md)  

User-defined stages of the lead processing workflow. Entity: Crm_Lead_User_Stages (Introduced in version 21.1.3.85)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Presales.LeadUserStages](Crm.Presales.LeadUserStages.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Presales.LeadUserStages.md#code) | string (32) | The unique code of the LeadUserStage. `Required` `Filter(eq;like)` `ORD` 
| [Description](Crm.Presales.LeadUserStages.md#description) | string (max) __nullable__ | Description of the user stage. Displayed to the end-user upon stage selection. 
| [Id](Crm.Presales.LeadUserStages.md#id) | guid |  
| [Name](Crm.Presales.LeadUserStages.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the user stage. `Required` `Filter(like)` 
| [Notes](Crm.Presales.LeadUserStages.md#notes) | string (max) __nullable__ | Notes for this LeadUserStage. 
| [SystemStage](Crm.Presales.LeadUserStages.md#systemstage) | [SystemStage](Crm.Presales.LeadUserStages.md#systemstage) | The system stage, on which the user stage is based. System stages are New, Qualifying, Marketing Qualified Lead, Sales Qualified Lead, Closed. (NEW, QUA, MQL, SQL, CLO). `Required` `Filter(multi eq)` 


## Attribute Details

### Code

The unique code of the LeadUserStage. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Description

Description of the user stage. Displayed to the end-user upon stage selection.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multi-language name of the user stage. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this LeadUserStage.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### SystemStage

The system stage, on which the user stage is based. System stages are New, Qualifying, Marketing Qualified Lead, Sales Qualified Lead, Closed. (NEW, QUA, MQL, SQL, CLO). `Required` `Filter(multi eq)`

_Type_: **[SystemStage](Crm.Presales.LeadUserStages.md#systemstage)**  
Allowed values for the `SystemStage`(Crm.Presales.Leads.md#systemstage) data attribute  
_Allowed Values (Crm.Presales.LeadsRepository.SystemStage Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 'NEW'. <br /> _Database Value:_ 'NEW' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Qualifying | Qualifying value. Stored as 'QUA'. <br /> _Database Value:_ 'QUA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Qualifying' |
| MarketingQualifiedLead | MarketingQualifiedLead value. Stored as 'MQL'. <br /> _Database Value:_ 'MQL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MarketingQualifiedLead' |
| SalesQualifiedLead | SalesQualifiedLead value. Stored as 'SQL'. <br /> _Database Value:_ 'SQL' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'SalesQualifiedLead' |
| Closed | Closed value. Stored as 'CLO'. <br /> _Database Value:_ 'CLO' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Presales.LeadUserStages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Presales.LeadUserStages erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_LeadUserStages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_LeadUserStages?$top=10>

