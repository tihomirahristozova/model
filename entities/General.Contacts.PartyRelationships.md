# General.Contacts.PartyRelationships

Defines the relationships between the parties. The data is preserved over time. Entity: Cm_Party_Relationships

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.PartyRelationships.md#Id) | guid |  
| [FromDate](General.Contacts.PartyRelationships.md#FromDate) | datetime (nullable) | The starting date of the relationship. null means the date is the begining of the time. [Filter(ge;le)] 
| [Notes](General.Contacts.PartyRelationships.md#Notes) | string (nullable) | Notes for this PartyRelationship. 
| [ToDate](General.Contacts.PartyRelationships.md#ToDate) | datetime (nullable) | The ending date of the relationship. null means the relationship is still active. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FromParty](General.Contacts.PartyRelationships.md#FromParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The first party in the relationship. [Required] [Filter(multi eq)] |
| [RelationshipType](General.Contacts.PartyRelationships.md#RelationshipType) | [General.Contacts.PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md) | The type of the relationship. [Required] [Filter(multi eq)] |
| [ToParty](General.Contacts.PartyRelationships.md#ToParty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The second party in the relationship. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> The starting date of the relationship. null means the date is the begining of the time. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

> Notes for this PartyRelationship.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDate

> The ending date of the relationship. null means the relationship is still active. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### FromParty

> The first party in the relationship. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RelationshipType

> The type of the relationship. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ToParty

> The second party in the relationship. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.PartyRelationships erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyRelationships erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.PartyRelationships erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyRelationships?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyRelationships?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Party_Relationships?$top=10>

