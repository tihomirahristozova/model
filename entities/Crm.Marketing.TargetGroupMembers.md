# Crm.Marketing.TargetGroupMembers

Member parties of a marketing target group. Entity: Crm_Target_Group_Members

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.TargetGroupMembers.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](Crm.Marketing.TargetGroupMembers.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The member party. [Required] [Filter(multi eq)] |
| [TargetGroup](Crm.Marketing.TargetGroupMembers.md#TargetGroup) | [Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md) | The target group, which includes the member party. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### Party

> The member party. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TargetGroup

> The target group, which includes the member party. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Marketing.TargetGroupMembers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.TargetGroupMembers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Marketing.TargetGroupMembers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_TargetGroupMembers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_TargetGroupMembers?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Target_Group_Members?$top=10>

