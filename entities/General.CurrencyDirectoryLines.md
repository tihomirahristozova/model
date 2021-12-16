---
uid: General.CurrencyDirectoryLines
---
# General.CurrencyDirectoryLines Entity

**Namespace:** [General](General.md)  

Contains exchange rate for a currency against the main currency of currency directory. Entity: Gen_Currency_Directory_Lines

## Default Visualization
Default Display Text Format:  
_{CurrencyDirectory.Name}_  
Default Search Members:  
_CurrencyDirectory.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.CurrencyDirectories](General.CurrencyDirectories.md)  
Aggregate Root:  
[General.CurrencyDirectories](General.CurrencyDirectories.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.CurrencyDirectoryLines.md#id) | guid |  
| [RateDivisor](General.CurrencyDirectoryLines.md#ratedivisor) | decimal (18, 6) | The divisor for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)` 
| [RateMultiplier](General.CurrencyDirectoryLines.md#ratemultiplier) | decimal (18, 6) | The multiplier for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)` 
| [RowVersion](General.CurrencyDirectoryLines.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CurrencyDirectory](General.CurrencyDirectoryLines.md#currencydirectory) | [CurrencyDirectories](General.CurrencyDirectories.md) | The <see cref="CurrencyDirectory"/> to which this CurrencyDirectoryLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [FromCurrency](General.CurrencyDirectoryLines.md#fromcurrency) | [Currencies](General.Currencies.md) | The currency for which the exchange rate is recorded. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### RateDivisor

The divisor for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)`

_Type_: **decimal (18, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### RateMultiplier

The multiplier for conversion from From_Currency to Directory.To_Currency. `Required` `Default(1)`

_Type_: **decimal (18, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CurrencyDirectory

The <see cref="CurrencyDirectory"/> to which this CurrencyDirectoryLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[CurrencyDirectories](General.CurrencyDirectories.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### FromCurrency

The currency for which the exchange rate is recorded. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.CurrencyDirectoryLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.CurrencyDirectoryLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_CurrencyDirectoryLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_CurrencyDirectoryLines?$top=10>

