---
uid: Communities.SocialGroups
---
# Communities.SocialGroups

Represents a group of users, sharing interest in the group topic. Entity: Cmm_Social_Groups (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.SocialGroups.md#Id) | guid |  
| [Notes](Communities.SocialGroups.md#Notes) | string (nullable) | Notes for this SocialGroup. 
| [Code](Communities.SocialGroups.md#Code) | string | Unique code of the group. Also used as group slug for Internet URL purposes. [Required] [ORD] 
| [Name](Communities.SocialGroups.md#Name) | string | Multilanguage name of the group. [Required] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [Communities.SocialGroupMembers](Communities.SocialGroupMembers.md) | List of [SocialGroupMember](Communities.SocialGroupMembers.md) child objects, based on the [Communities.SocialGroupMember.SocialGroup](Communities.SocialGroupMembers.md#SocialGroup) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this SocialGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Unique code of the group. Also used as group slug for Internet URL purposes. [Required] [ORD]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the group. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Communities.SocialGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.SocialGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialGroups?$top=10>

