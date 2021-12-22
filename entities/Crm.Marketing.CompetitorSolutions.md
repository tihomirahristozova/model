---
uid: Crm.Marketing.CompetitorSolutions
---
# Crm.Marketing.CompetitorSolutions Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

The solutions offered by a competitor. Entity: Crm_Competitor_Solutions (Introduced in version 22.1.4.70)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Marketing.Competitors](Crm.Marketing.Competitors.md)  
Aggregate Root:  
[Crm.Marketing.Competitors](Crm.Marketing.Competitors.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.CompetitorSolutions.md#id) | guid |  
| [Name](Crm.Marketing.CompetitorSolutions.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language string. `Required` `Filter(like)` 
| [Notes](Crm.Marketing.CompetitorSolutions.md#notes) | string (max) __nullable__ | Notes for this CompetitorSolution. 
| [ObjectVersion](Crm.Marketing.CompetitorSolutions.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanySizeClass](Crm.Marketing.CompetitorSolutions.md#companysizeclass) | [CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable) | When not null, specifies the company size, for which the solution is targeted. `Filter(multi eq)` |
| [Competitor](Crm.Marketing.CompetitorSolutions.md#competitor) | [Competitors](Crm.Marketing.Competitors.md) | Competitor to our marketing solutions. `Required` `Filter(multi eq)` `Owner` |
| [Industry](Crm.Marketing.CompetitorSolutions.md#industry) | [Industries](Crm.Marketing.Industries.md) (nullable) | When not null, specifies the industry, for which the solution is targeted. `Filter(multi eq)` |
| [OurMarketingSolution](Crm.Marketing.CompetitorSolutions.md#ourmarketingsolution) | [MarketingSolutions](Crm.Marketing.MarketingSolutions.md) (nullable) | Our marketing solution, which is competing with the competitor solution. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multi-language string. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this CompetitorSolution.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### CompanySizeClass

When not null, specifies the company size, for which the solution is targeted. `Filter(multi eq)`

_Type_: **[CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Competitor

Competitor to our marketing solutions. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Competitors](Crm.Marketing.Competitors.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Industry

When not null, specifies the industry, for which the solution is targeted. `Filter(multi eq)`

_Type_: **[Industries](Crm.Marketing.Industries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### OurMarketingSolution

Our marketing solution, which is competing with the competitor solution. `Filter(multi eq)`

_Type_: **[MarketingSolutions](Crm.Marketing.MarketingSolutions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.CompetitorSolutions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.CompetitorSolutions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_CompetitorSolutions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_CompetitorSolutions?$top=10>

