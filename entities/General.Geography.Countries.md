---
uid: General.Geography.Countries
---
# General.Geography.Countries Entity

**Namespace:** [General.Geography](General.Geography.md)  

List of countries, listed by their internet suffix code. Entity: Gen_Countries

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [General.Geography.Countries](General.Geography.Countries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Geography.Countries.md#code) | string | Internet suffix code of the country. [Required] [Filter(eq;like)] [ORD] 
| [Id](General.Geography.Countries.md#id) | guid |  
| [IntrastatCode](General.Geography.Countries.md#intrastatcode) | string (nullable) | This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. [Introduced in version 20.1] 
| [Name](General.Geography.Countries.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the country. [Required] [Filter(like)] 


## Attribute Details

### Code

Internet suffix code of the country. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IntrastatCode

This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. [Introduced in version 20.1]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

Name of the country. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Geography.Countries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Geography.Countries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_Countries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_Countries?$top=10>

