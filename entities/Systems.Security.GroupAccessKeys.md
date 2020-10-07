# Systems.Security.GroupAccessKeys

Specifies the access keys for which the user groups have permissions. The existance of a record grants read permission. Additional permissions are granted through specialized fields. Entity: Sec_Group_Access_Keys

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.GroupAccessKeys.md#Id) | guid |  
| [CanAdminister](Systems.Security.GroupAccessKeys.md#CanAdminister) | boolean | When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key. [Required] [Default(false)] 
| [CanDelete](Systems.Security.GroupAccessKeys.md#CanDelete) | boolean | When true, the group is granted with delete permission for the entity, protected by the access key. [Required] 
| [CanUpdate](Systems.Security.GroupAccessKeys.md#CanUpdate) | boolean | When true, the group is granted with update permission for the entity, protected by the access key. [Required] 
| [Permission1](Systems.Security.GroupAccessKeys.md#Permission1) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission10](Systems.Security.GroupAccessKeys.md#Permission10) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission2](Systems.Security.GroupAccessKeys.md#Permission2) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission3](Systems.Security.GroupAccessKeys.md#Permission3) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission4](Systems.Security.GroupAccessKeys.md#Permission4) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission5](Systems.Security.GroupAccessKeys.md#Permission5) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission6](Systems.Security.GroupAccessKeys.md#Permission6) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission7](Systems.Security.GroupAccessKeys.md#Permission7) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission8](Systems.Security.GroupAccessKeys.md#Permission8) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 
| [Permission9](Systems.Security.GroupAccessKeys.md#Permission9) | boolean | When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.GroupAccessKeys.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) | This access key, to which we are granting access permissions. [Required] [Filter(multi eq)] |
| [Group](Systems.Security.GroupAccessKeys.md#Group) | [Systems.Security.Groups](Systems.Security.Groups.md) | The group, which is granted with access permission. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CanAdminister

> When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CanDelete

> When true, the group is granted with delete permission for the entity, protected by the access key. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CanUpdate

> When true, the group is granted with update permission for the entity, protected by the access key. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Permission1

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission10

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission2

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission3

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission4

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission5

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission6

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission7

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission8

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission9

> When true, the group is granted with entity-specific permission for the entity, protected by the access key. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### AccessKey

> This access key, to which we are granting access permissions. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Group

> The group, which is granted with access permission. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Security.Groups](Systems.Security.Groups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.GroupAccessKeys erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.GroupAccessKeys erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.GroupAccessKeys erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_GroupAccessKeys?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_GroupAccessKeys?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_Group_Access_Keys?$top=10>

