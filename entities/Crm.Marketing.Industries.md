---
uid: Crm.Marketing.Industries
---
# Crm.Marketing.Industries Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

The industries, for which we are offering solutions. Entity: Crm_Industries (Introduced in version 21.1.3.59)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.Industries](Crm.Marketing.Industries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Marketing.Industries.md#code) | string (32) | The unique code of the Industry. `Required` `Filter(eq;like)` `ORD` 
| [Id](Crm.Marketing.Industries.md#id) | guid |  
| [Name](Crm.Marketing.Industries.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Industry name (multi-language). `Required` `Filter(eq;like)` 
| [Notes](Crm.Marketing.Industries.md#notes) | string (max) __nullable__ | Notes for this Industry. 
| [ObjectVersion](Crm.Marketing.Industries.md#objectversion) | int32 |  


## Attribute Details

### Code

The unique code of the Industry. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Industry name (multi-language). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Industry.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.Industries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.Industries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_Industries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_Industries?$top=10>

