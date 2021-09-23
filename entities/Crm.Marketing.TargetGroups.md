---
uid: Crm.Marketing.TargetGroups
---
# Crm.Marketing.TargetGroups Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Marketing target group, containing a fixed list of parties. Entity: Crm_Target_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md)  
  * [Crm.Marketing.TargetGroupMembers](Crm.Marketing.TargetGroupMembers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Marketing.TargetGroups.md#code) | string (16) | Short code for identification of target groups. `Required` `Filter(eq;like)` `ORD` 
| [Description](Crm.Marketing.TargetGroups.md#description) | string (254) __nullable__ | The description of this TargetGroup. 
| [Id](Crm.Marketing.TargetGroups.md#id) | guid |  
| [Name](Crm.Marketing.TargetGroups.md#name) | string (64) | The name of this TargetGroup. `Required` `Filter(like)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [TargetGroupMembers](Crm.Marketing.TargetGroupMembers.md) | List of `TargetGroupMember`(Crm.Marketing.TargetGroupMembers.md) child objects, based on the `Crm.Marketing.TargetGroupMember.TargetGroup`(Crm.Marketing.TargetGroupMembers.md#targetgroup) back reference 


## Attribute Details

### Code

Short code for identification of target groups. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Description

The description of this TargetGroup.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this TargetGroup. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.TargetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.TargetGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_TargetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_TargetGroups?$top=10>

