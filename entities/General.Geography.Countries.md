---
uid: General.Geography.Countries
---
# General.Geography.Countries Entity

**Namespace:** [General.Geography](General.Geography.md)  

List of countries, listed by their internet suffix code. Entity: Gen_Countries

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Geography.Countries](General.Geography.Countries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Geography.Countries.md#code) | string (2) | Internet suffix code of the country. `Required` `Filter(eq;like)` `ORD` 
| [Id](General.Geography.Countries.md#id) | guid |  
| [IntrastatCode](General.Geography.Countries.md#intrastatcode) | string (2) __nullable__ | This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. `Introduced in version 20.1` 
| [Name](General.Geography.Countries.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the country. `Required` `Filter(like)` 
| [ObjectVersion](General.Geography.Countries.md#objectversion) | int32 |  


## Attribute Details

### Code

Internet suffix code of the country. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (2)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **2**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IntrastatCode

This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. `Introduced in version 20.1`

_Type_: **string (2) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2**  

### Name

Name of the country. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  



## Business Rules

[!list limit=1000 erp.entity=General.Geography.Countries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Geography.Countries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_Countries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_Countries?$top=10>

