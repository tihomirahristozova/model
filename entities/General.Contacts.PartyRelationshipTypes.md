# General.Contacts.PartyRelationshipTypes

Defines the types of relationships possible between the parties. Entity: Cm_Party_Relationship_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.PartyRelationshipTypes.md#Id) | guid |  
| [Notes](General.Contacts.PartyRelationshipTypes.md#Notes) | string (nullable) | Notes for this PartyRelationshipType. 
| [RelationshipTypeName](General.Contacts.PartyRelationshipTypes.md#RelationshipTypeName) | string | The name of the relationship type. [Required] [Filter(like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this PartyRelationshipType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RelationshipTypeName

> The name of the relationship type. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.PartyRelationshipTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyRelationshipTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.PartyRelationshipTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyRelationshipTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyRelationshipTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Party_Relationship_Types?$top=10>

