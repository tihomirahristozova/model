---
uid: General.PropertiesCategories
---
# General.PropertiesCategories Entity

**Namespace:** [General](General.md)  

Categories of properties. Entity: Gen_Properties_Categories

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.PropertiesCategories](General.PropertiesCategories.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PropertiesCategories.md#id) | guid |  
| [Name](General.PropertiesCategories.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this PropertiesCategory. `Required` `Filter(eq;like)` `ORD` 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PropertiesCategory. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.PropertiesCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.PropertiesCategories erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertiesCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertiesCategories?$top=10>

