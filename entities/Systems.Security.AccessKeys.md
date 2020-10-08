---
uid: Systems.Security.AccessKeys
---
# Systems.Security.AccessKeys

Access keys provide the basic locking mechanism for data security. Each record can be secured by specifying an access key. Then the users are given access to access keys through groups. Entity: Sec_Access_Keys

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.AccessKeys.md#Id) | guid |  
| [Code](Systems.Security.AccessKeys.md#Code) | string (nullable) | Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries. [Filter(eq;like)] 
| [Name](Systems.Security.AccessKeys.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | Multilanguage descriptive name of the security key. Can be null for legacy keys. [Filter(eq;like)] 
| [EntityName](Systems.Security.AccessKeys.md#EntityName) | string (nullable) | What entitity the key secures. Can be null for private, legacy keys. [Filter(eq;like)] [ORD] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Multilanguage descriptive name of the security key. Can be null for legacy keys. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### EntityName

> What entitity the key secures. Can be null for private, legacy keys. [Filter(eq;like)] [ORD]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=Systems.Security.AccessKeys erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.AccessKeys erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.AccessKeys erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_AccessKeys?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_AccessKeys?$top=10>

