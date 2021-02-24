---
uid: Communities.SocialGroups
---
# Communities.SocialGroups Entity

Represents a group of users, sharing interest in the group topic. Entity: Cmm_Social_Groups (Introduced in version 20.1)

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## [Aggregate Tree](xref:aggregates)  
* [Communities.SocialGroups](Communities.SocialGroups.md)  
  * [Communities.SocialGroupMembers](Communities.SocialGroupMembers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Communities.SocialGroups.md#code) | string | Unique code of the group. Also used as group slug for Internet URL purposes. [Required] [ORD] 
| [Id](Communities.SocialGroups.md#id) | guid |  
| [Name](Communities.SocialGroups.md#name) | string | Multilanguage name of the group. [Required] 
| [Notes](Communities.SocialGroups.md#notes) | string (nullable) | Notes for this SocialGroup. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [SocialGroupMembers](Communities.SocialGroupMembers.md) | List of [SocialGroupMember](Communities.SocialGroupMembers.md) child objects, based on the [Communities.SocialGroupMember.SocialGroup](Communities.SocialGroupMembers.md#socialgroup) back reference 


## Attribute Details

### Code

Unique code of the group. Also used as group slug for Internet URL purposes. [Required] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage name of the group. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this SocialGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Communities.SocialGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialGroups?$top=10>

