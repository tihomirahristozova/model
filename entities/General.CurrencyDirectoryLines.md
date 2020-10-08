---
uid: General.CurrencyDirectoryLines
---
# General.CurrencyDirectoryLines

Contains exchange rate for a currency against the main currency of currency directory. Entity: Gen_Currency_Directory_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.CurrencyDirectoryLines.md#Id) | guid |  
| [RateDivisor](General.CurrencyDirectoryLines.md#RateDivisor) | decimal | The divisor for conversion from From_Currency to Directory.To_Currency. [Required] [Default(1)] 
| [RateMultiplier](General.CurrencyDirectoryLines.md#RateMultiplier) | decimal | The multiplier for conversion from From_Currency to Directory.To_Currency. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CurrencyDirectory](General.CurrencyDirectoryLines.md#CurrencyDirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) | The [CurrencyDirectory](General.CurrencyDirectoryLines.md#CurrencyDirectory) to which this CurrencyDirectoryLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [FromCurrency](General.CurrencyDirectoryLines.md#FromCurrency) | [General.Currencies](General.Currencies.md) | The currency for which the exchange rate is recorded. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### RateDivisor

> The divisor for conversion from From_Currency to Directory.To_Currency. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### RateMultiplier

> The multiplier for conversion from From_Currency to Directory.To_Currency. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### CurrencyDirectory

> The [CurrencyDirectory](General.CurrencyDirectoryLines.md#CurrencyDirectory) to which this CurrencyDirectoryLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.CurrencyDirectories](General.CurrencyDirectories.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### FromCurrency

> The currency for which the exchange rate is recorded. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.CurrencyDirectoryLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.CurrencyDirectoryLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.CurrencyDirectoryLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_CurrencyDirectoryLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_CurrencyDirectoryLines?$top=10>

