---
uid: Crm.Marketing.TargetGroups
---
# Crm.Marketing.TargetGroups

Marketing target group, containing a fixed list of parties. Entity: Crm_Target_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.TargetGroups.md#Id) | guid |  
| [Description](Crm.Marketing.TargetGroups.md#Description) | string (nullable) | The description of this TargetGroup. 
| [Code](Crm.Marketing.TargetGroups.md#Code) | string | Short code for identification of target groups. [Required] [Filter(eq;like)] [ORD] 
| [Name](Crm.Marketing.TargetGroups.md#Name) | string | The name of this TargetGroup. [Required] [Filter(like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [Crm.Marketing.TargetGroupMembers](Crm.Marketing.TargetGroupMembers.md) | List of [TargetGroupMember](Crm.Marketing.TargetGroupMembers.md) child objects, based on the [Crm.Marketing.TargetGroupMember.TargetGroup](Crm.Marketing.TargetGroupMembers.md#TargetGroup) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this TargetGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Short code for identification of target groups. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> The name of this TargetGroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Marketing.TargetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.TargetGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Marketing.TargetGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_TargetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_TargetGroups?$top=10>

