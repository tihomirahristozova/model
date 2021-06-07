---
uid: Systems.Security.UserProviderTokens
---
# Systems.Security.UserProviderTokens Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Stores verification tokens for users - e.g. tokens for email, phone or two-factor authentication. Entity: Sec_User_Provider_Tokens (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{LoginProviderName:T}_  
Default Search Member:  
_LoginProviderName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Security.Users](Systems.Security.Users.md)  
Aggregate Root:  
[Systems.Security.Users](Systems.Security.Users.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.UserProviderTokens.md#id) | guid |  
| [LoginProviderName](Systems.Security.UserProviderTokens.md#loginprovidername) | string (450) | Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc. `Required` `Filter(eq)` 
| [TokenName](Systems.Security.UserProviderTokens.md#tokenname) | string (450) | What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery). `Required` `Filter(eq)` 
| [TokenValue](Systems.Security.UserProviderTokens.md#tokenvalue) | string (max) __nullable__ | Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Systems.Security.UserProviderTokens.md#user) | [Users](Systems.Security.Users.md) | User for which we store tokens. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LoginProviderName

Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc. `Required` `Filter(eq)`

_Type_: **string (450)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **450**  

### TokenName

What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery). `Required` `Filter(eq)`

_Type_: **string (450)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **450**  

### TokenValue

Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### User

User for which we store tokens. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Systems.Security.UserProviderTokens erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.UserProviderTokens erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserProviderTokens?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserProviderTokens?$top=10>

