---
uid: Crm.Marketing.TargetGroupMembers
---
# Crm.Marketing.TargetGroupMembers Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Member parties of a marketing target group. Entity: Crm_Target_Group_Members

## Default Visualization
Default Display Text Format:  
_{TargetGroup.Name:T} : {TargetGroup.Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md)  
Aggregate Root:  
[Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.TargetGroupMembers.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](Crm.Marketing.TargetGroupMembers.md#party) | [Parties](General.Contacts.Parties.md) | The member party. `Required` `Filter(multi eq)` |
| [TargetGroup](Crm.Marketing.TargetGroupMembers.md#targetgroup) | [TargetGroups](Crm.Marketing.TargetGroups.md) | The target group, which includes the member party. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Party

The member party. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### TargetGroup

The target group, which includes the member party. `Required` `Filter(multi eq)` `Owner`

_Type_: **[TargetGroups](Crm.Marketing.TargetGroups.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.TargetGroupMembers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.TargetGroupMembers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_TargetGroupMembers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_TargetGroupMembers?$top=10>

