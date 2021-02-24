---
uid: Systems.Security.AccessKeys
---
# Systems.Security.AccessKeys Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Access keys provide the basic locking mechanism for data security. Each record can be secured by specifying an access key. Then the users are given access to access keys through groups. Entity: Sec_Access_Keys

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Systems.Security.AccessKeys.md#code) | string (nullable) | Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries. [Filter(eq;like)] 
| [EntityName](Systems.Security.AccessKeys.md#entityname) | string (nullable) | What entitity the key secures. Can be null for private, legacy keys. [Filter(eq;like)] [ORD] 
| [Id](Systems.Security.AccessKeys.md#id) | guid |  
| [Name](Systems.Security.AccessKeys.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Multilanguage descriptive name of the security key. Can be null for legacy keys. [Filter(eq;like)] 


## Attribute Details

### Code

Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### EntityName

What entitity the key secures. Can be null for private, legacy keys. [Filter(eq;like)] [ORD]

_Type_: **string (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage descriptive name of the security key. Can be null for legacy keys. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.AccessKeys erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.AccessKeys erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_AccessKeys?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_AccessKeys?$top=10>

