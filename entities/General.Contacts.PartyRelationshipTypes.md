---
uid: General.Contacts.PartyRelationshipTypes
---
# General.Contacts.PartyRelationshipTypes Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Defines the types of relationships possible between the parties. Entity: Cm_Party_Relationship_Types

## Default Visualization
Default Display Text Format:  
_{RelationshipTypeName:T}_  
Default Search Member:  
_RelationshipTypeName_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [General.Contacts.PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.PartyRelationshipTypes.md#id) | guid |  
| [Notes](General.Contacts.PartyRelationshipTypes.md#notes) | string (nullable) | Notes for this PartyRelationshipType. 
| [RelationshipTypeName](General.Contacts.PartyRelationshipTypes.md#relationshiptypename) | string | The name of the relationship type. [Required] [Filter(like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this PartyRelationshipType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RelationshipTypeName

The name of the relationship type. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.PartyRelationshipTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyRelationshipTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyRelationshipTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyRelationshipTypes?$top=10>

