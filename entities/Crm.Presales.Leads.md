---
uid: Crm.Presales.Leads
---
# Crm.Presales.Leads Entity

**Namespace:** [Crm.Presales](Crm.Presales.md)  

Leads are potential customers for your products. Because leads are usually processed in a hurry or imported from external lists, personal and company information is saved in a less structured way. With the advancement of the qualification process (including deduplication), the information is structured in the usual Person and Company entities. When successfully processed, leads can be converted to Opportunities. Entity: Crm_Leads (Introduced in version 21.1.3.78)

## Default Visualization
Default Display Text Format:  
_{CompanyName:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Presales.Leads](Crm.Presales.Leads.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanyName](Crm.Presales.Leads.md#companyname) | string (64) __nullable__ | The name of the company, which the person works for (in relation to the current lead). `Filter(eq;like)` 
| [CreationTimestampUtc](Crm.Presales.Leads.md#creationtimestamputc) | datetime | System assigned date and time (in UTC), when the lead was initially created. `Required` `Filter(ge;le)` `ReadOnly` 
| [Id](Crm.Presales.Leads.md#id) | guid |  
| [MQLTimestampUtc](Crm.Presales.Leads.md#mqltimestamputc) | datetime __nullable__ | System assigned date and time (in UTC), when the lead was first promoted to Marketing Qualified Lead (MQL). `Filter(ge;le)` `ReadOnly` 
| [PersonEmail](Crm.Presales.Leads.md#personemail) | string (64) __nullable__ | The email address of the sales lead person. `Filter(eq;like)` 
| [PersonFirstName](Crm.Presales.Leads.md#personfirstname) | string (64) __nullable__ | The first name of the person, representing the sales lead. `Filter(eq;like)` 
| [PersonLastName](Crm.Presales.Leads.md#personlastname) | string (64) __nullable__ | The last name of the person, representing the sales lead. `Filter(eq;like)` 
| [PersonMobilePhone](Crm.Presales.Leads.md#personmobilephone) | string (32) __nullable__ | The mobile phone of the sales lead person. `Filter(like)` 
| [PersonSalutation](Crm.Presales.Leads.md#personsalutation) | string (16) __nullable__ | Salutation for the sales lead person. `Filter(eq;like)` 
| [PersonWebProfile](Crm.Presales.Leads.md#personwebprofile) | string (64) __nullable__ | Web address (including protocol like https) of the personal profile in a social or professional network. The address itself, as it is full valid Internet address, contains also the network name. `Filter(like)` 
| [PersonWorkPhone](Crm.Presales.Leads.md#personworkphone) | string (32) __nullable__ | The work phone of the sales lead person. `Filter(like)` 
| [RoleInCompany](Crm.Presales.Leads.md#roleincompany) | string (32) __nullable__ | The role of the person in the company. `Filter(eq;like)` 
| [SQLTimestampUtc](Crm.Presales.Leads.md#sqltimestamputc) | datetime __nullable__ | System assigned date and time (in UTC), when the lead was first promoted to Sales Qualified Lead. `Filter(ge;le)` `ReadOnly` 
| [SystemStage](Crm.Presales.Leads.md#systemstage) | [SystemStage](Crm.Presales.Leads.md#systemstage) | The system stage of the lead - New, Qualifying, Marketing Qualified Lead, Sales Qualified Lead, Closed. (NEW, QUA, MQL, SQL, CLO). `Required` `Default("NEW")` `Filter(multi eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssignedToSalesPerson](Crm.Presales.Leads.md#assignedtosalesperson) | [SalesPersons](Crm.SalesPersons.md) (nullable) | Sales rep to whom this lead is assigned for further processing. null - not yet assigned. `Filter(multi eq)` |
| [Campaign](Crm.Presales.Leads.md#campaign) | [Campaigns](Crm.Marketing.Campaigns.md) | The marketing campaign under which the lead was generated. `Required` `Filter(multi eq)` |
| [ConvertedToDeal](Crm.Presales.Leads.md#convertedtodeal) | [Deals](Crm.Presales.Deals.md) (nullable) | Filled when the lead is converted to opportunity (deal). `Filter(multi eq)` |
| [IdentifiedCompany](Crm.Presales.Leads.md#identifiedcompany) | [Companies](General.Contacts.Companies.md) (nullable) | Filled when the company is identified within our database. `Filter(multi eq)` |
| [IdentifiedPerson](Crm.Presales.Leads.md#identifiedperson) | [Persons](General.Contacts.Persons.md) (nullable) | Filled when the person is identified and recorded in our master records. `Filter(multi eq)` |
| [LeadUserStage](Crm.Presales.Leads.md#leaduserstage) | [LeadUserStages](Crm.Presales.LeadUserStages.md) (nullable) | The user-defined sub-stage of the lead. This also defines the step in the sales sequence and the next appropriate activity to engage the lead. null when the user stage is undefined (the pure System Stage defines the stage). `Filter(multi eq)` |
| [MarketingCompanySize](Crm.Presales.Leads.md#marketingcompanysize) | [CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable) | The size class of the company. `Filter(multi eq)` |
| [MarketingIndustry](Crm.Presales.Leads.md#marketingindustry) | [Industries](Crm.Marketing.Industries.md) (nullable) | The industry (for marketing purposes) of the lead. `Filter(multi eq)` |
| [MarketingSolution](Crm.Presales.Leads.md#marketingsolution) | [MarketingSolutions](Crm.Marketing.MarketingSolutions.md) (nullable) | The marketing solution, in which the lead is interested or which generated the lead. `Filter(multi eq)` |
| [OwnerUser](Crm.Presales.Leads.md#owneruser) | [Users](Systems.Security.Users.md) | The user, responsible for this record. `Required` `Filter(multi eq)` |
| [SalesArea](Crm.Presales.Leads.md#salesarea) | [Areas](General.Geography.Areas.md) (nullable) | The sales area, where the lead is located, when it is identified. This should also indicate the Time Zone. `Filter(multi eq)` |


## Attribute Details

### CompanyName

The name of the company, which the person works for (in relation to the current lead). `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### CreationTimestampUtc

System assigned date and time (in UTC), when the lead was initially created. `Required` `Filter(ge;le)` `ReadOnly`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( obj.MQLTimestampUtc == null), Convert( DateTime.UtcNow, Nullable`1), obj.MQLTimestampUtc)`

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MQLTimestampUtc

System assigned date and time (in UTC), when the lead was first promoted to Marketing Qualified Lead (MQL). `Filter(ge;le)` `ReadOnly`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PersonEmail

The email address of the sales lead person. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PersonFirstName

The first name of the person, representing the sales lead. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PersonLastName

The last name of the person, representing the sales lead. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PersonMobilePhone

The mobile phone of the sales lead person. `Filter(like)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### PersonSalutation

Salutation for the sales lead person. `Filter(eq;like)`

_Type_: **string (16) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### PersonWebProfile

Web address (including protocol like https) of the personal profile in a social or professional network. The address itself, as it is full valid Internet address, contains also the network name. `Filter(like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PersonWorkPhone

The work phone of the sales lead person. `Filter(like)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### RoleInCompany

The role of the person in the company. `Filter(eq;like)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### SQLTimestampUtc

System assigned date and time (in UTC), when the lead was first promoted to Sales Qualified Lead. `Filter(ge;le)` `ReadOnly`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### SystemStage

The system stage of the lead - New, Qualifying, Marketing Qualified Lead, Sales Qualified Lead, Closed. (NEW, QUA, MQL, SQL, CLO). `Required` `Default("NEW")` `Filter(multi eq)`

_Type_: **[SystemStage](Crm.Presales.Leads.md#systemstage)**  
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
_Default Value_: **New**  


## Reference Details

### AssignedToSalesPerson

Sales rep to whom this lead is assigned for further processing. null - not yet assigned. `Filter(multi eq)`

_Type_: **[SalesPersons](Crm.SalesPersons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Campaign

The marketing campaign under which the lead was generated. `Required` `Filter(multi eq)`

_Type_: **[Campaigns](Crm.Marketing.Campaigns.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ConvertedToDeal

Filled when the lead is converted to opportunity (deal). `Filter(multi eq)`

_Type_: **[Deals](Crm.Presales.Deals.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### IdentifiedCompany

Filled when the company is identified within our database. `Filter(multi eq)`

_Type_: **[Companies](General.Contacts.Companies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### IdentifiedPerson

Filled when the person is identified and recorded in our master records. `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### LeadUserStage

The user-defined sub-stage of the lead. This also defines the step in the sales sequence and the next appropriate activity to engage the lead. null when the user stage is undefined (the pure System Stage defines the stage). `Filter(multi eq)`

_Type_: **[LeadUserStages](Crm.Presales.LeadUserStages.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### MarketingCompanySize

The size class of the company. `Filter(multi eq)`

_Type_: **[CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### MarketingIndustry

The industry (for marketing purposes) of the lead. `Filter(multi eq)`

_Type_: **[Industries](Crm.Marketing.Industries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### MarketingSolution

The marketing solution, in which the lead is interested or which generated the lead. `Filter(multi eq)`

_Type_: **[MarketingSolutions](Crm.Marketing.MarketingSolutions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### OwnerUser

The user, responsible for this record. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesArea

The sales area, where the lead is located, when it is identified. This should also indicate the Time Zone. `Filter(multi eq)`

_Type_: **[Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Presales.Leads erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Presales.Leads erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_Leads?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_Leads?$top=10>

