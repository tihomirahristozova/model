# Systems.Security.UserAccessKeys

Obsolete. Not used. Entity: Sec_User_Access_Keys

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.UserAccessKeys.md#Id) | guid |  
| [CanDelete](Systems.Security.UserAccessKeys.md#CanDelete) | boolean | Obsolete. Not used. [Required] 
| [CanUpdate](Systems.Security.UserAccessKeys.md#CanUpdate) | boolean | Obsolete. Not used. [Required] 
| [Permission1](Systems.Security.UserAccessKeys.md#Permission1) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission10](Systems.Security.UserAccessKeys.md#Permission10) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission2](Systems.Security.UserAccessKeys.md#Permission2) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission3](Systems.Security.UserAccessKeys.md#Permission3) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission4](Systems.Security.UserAccessKeys.md#Permission4) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission5](Systems.Security.UserAccessKeys.md#Permission5) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission6](Systems.Security.UserAccessKeys.md#Permission6) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission7](Systems.Security.UserAccessKeys.md#Permission7) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission8](Systems.Security.UserAccessKeys.md#Permission8) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Permission9](Systems.Security.UserAccessKeys.md#Permission9) | boolean | Obsolete. Not used. [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.UserAccessKeys.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) | The access key, containing the user permissions for this UserAccessKey. Null means that all users have unlimited permissions. [Required] [Filter(multi eq)] |
| [User](Systems.Security.UserAccessKeys.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | Obsolete. Not used. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CanDelete

> Obsolete. Not used. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CanUpdate

> Obsolete. Not used. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Permission1

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission10

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission2

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission3

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission4

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission5

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission6

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission7

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission8

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission9

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this UserAccessKey. Null means that all users have unlimited permissions. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> Obsolete. Not used. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.UserAccessKeys erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.UserAccessKeys erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.UserAccessKeys erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserAccessKeys?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserAccessKeys?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_User_Access_Keys?$top=10>

