---
uid: Communities.SocialGroups
---
# Communities.SocialGroups Entity

**Namespace:** [Communities](Communities.md)  

Represents a group of users, sharing interest in the group topic. Entity: Cmm_Social_Groups (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Code; Name_  
Code Data Member:  
_Code_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Communities.SocialGroups](Communities.SocialGroups.md)  
  * [Communities.SocialGroupMembers](Communities.SocialGroupMembers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Communities.SocialGroups.md#code) | string (32) | Unique code of the group. Also used as group slug for Internet URL purposes. `Required` `ORD` 
| [DisplayText](Communities.SocialGroups.md#displaytext) | string |  
| [Id](Communities.SocialGroups.md#id) | guid |  
| [Name](Communities.SocialGroups.md#name) | string (256) | Multilanguage name of the group. `Required` 
| [Notes](Communities.SocialGroups.md#notes) | string (max) __nullable__ | Notes for this SocialGroup. 
| [ObjectVersion](Communities.SocialGroups.md#objectversion) | int32 |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [SocialGroupMembers](Communities.SocialGroupMembers.md) | List of `SocialGroupMember`(Communities.SocialGroupMembers.md) child objects, based on the `Communities.SocialGroupMember.SocialGroup`(Communities.SocialGroupMembers.md#socialgroup) back reference 


## Attribute Details

### Code

Unique code of the group. Also used as group slug for Internet URL purposes. `Required` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage name of the group. `Required`

_Type_: **string (256)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Notes

Notes for this SocialGroup.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

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

[!list limit=1000 erp.entity=Communities.SocialGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Communities.SocialGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialGroups?$top=10>

