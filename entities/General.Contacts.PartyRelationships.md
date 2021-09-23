---
uid: General.Contacts.PartyRelationships
---
# General.Contacts.PartyRelationships Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Defines the relationships between the parties. The data is preserved over time. Entity: Cm_Party_Relationships

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Contacts.PartyRelationships](General.Contacts.PartyRelationships.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](General.Contacts.PartyRelationships.md#fromdate) | datetime __nullable__ | The starting date of the relationship. null means the date is the begining of the time. `Filter(ge;le)` 
| [Id](General.Contacts.PartyRelationships.md#id) | guid |  
| [Notes](General.Contacts.PartyRelationships.md#notes) | string (254) __nullable__ | Notes for this PartyRelationship. 
| [ToDate](General.Contacts.PartyRelationships.md#todate) | datetime __nullable__ | The ending date of the relationship. null means the relationship is still active. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FromParty](General.Contacts.PartyRelationships.md#fromparty) | [Parties](General.Contacts.Parties.md) | The first party in the relationship. `Required` `Filter(multi eq)` |
| [RelationshipType](General.Contacts.PartyRelationships.md#relationshiptype) | [PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md) | The type of the relationship. `Required` `Filter(multi eq)` |
| [ToParty](General.Contacts.PartyRelationships.md#toparty) | [Parties](General.Contacts.Parties.md) | The second party in the relationship. `Required` `Filter(multi eq)` |


## Attribute Details

### FromDate

The starting date of the relationship. null means the date is the begining of the time. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this PartyRelationship.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ToDate

The ending date of the relationship. null means the relationship is still active. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### FromParty

The first party in the relationship. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RelationshipType

The type of the relationship. `Required` `Filter(multi eq)`

_Type_: **[PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToParty

The second party in the relationship. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Contacts.PartyRelationships erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.PartyRelationships erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyRelationships?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyRelationships?$top=10>

