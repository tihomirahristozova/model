---
uid: Systems.Security.Domains
---
# Systems.Security.Domains Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Represents one user domain. The users in a domain have different emails. But one user can use the same email to register in different domains. Entity: Sec_Domains (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.Domains](Systems.Security.Domains.md)  
  * [Systems.Security.DomainProviders](Systems.Security.DomainProviders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowLocalAccounts](Systems.Security.Domains.md#allowlocalaccounts) | boolean | Specifies whether users can have local accounts with locally stored passwords in the DB (not recommended). `Required` `Default(true)` 
| [Description](Systems.Security.Domains.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | Multi-language description of the domain. 
| [Id](Systems.Security.Domains.md#id) | guid |  
| [IsDefault](Systems.Security.Domains.md#isdefault) | boolean | Specifies whether this is the default domain for the database. `Required` `Default(true)` `Filter(eq)` 
| [Name](Systems.Security.Domains.md#name) | string (64) | The name of the domain (restricted for URL usage). `Required` `Filter(eq;like)` `ORD` 
| [ObjectVersion](Systems.Security.Domains.md#objectversion) | int32 |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Providers | [DomainProviders](Systems.Security.DomainProviders.md) | List of `DomainProvider`(Systems.Security.DomainProviders.md) child objects, based on the `Systems.Security.DomainProvider.Domain`(Systems.Security.DomainProviders.md#domain) back reference 


## Attribute Details

### AllowLocalAccounts

Specifies whether users can have local accounts with locally stored passwords in the DB (not recommended). `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Description

Multi-language description of the domain.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

Specifies whether this is the default domain for the database. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of the domain (restricted for URL usage). `Required` `Filter(eq;like)` `ORD`

_Type_: **string (64)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.Domains erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.Domains erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_Domains?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_Domains?$top=10>

