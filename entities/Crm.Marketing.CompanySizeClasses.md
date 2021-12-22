---
uid: Crm.Marketing.CompanySizeClasses
---
# Crm.Marketing.CompanySizeClasses Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Categorization of company sizes for marketing purposes. Size classes might depend on number of employees, annual revenue and/or other factors (expresses as user defined attributes). Entity: Crm_Company_Size_Classes (Introduced in version 21.1.3.59)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.CompanySizeClasses](Crm.Marketing.CompanySizeClasses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Marketing.CompanySizeClasses.md#code) | string (32) | The unique code of the CompanySizeClass. `Required` `Filter(eq;like)` `ORD` 
| [FromEmployees](Crm.Marketing.CompanySizeClasses.md#fromemployees) | int32 __nullable__ | Minimal number of employees for this size class. null if this is not relevant to this size class. `Filter(eq)` 
| [FromRevenue](Crm.Marketing.CompanySizeClasses.md#fromrevenue) | decimal (15, 0) __nullable__ | Minimal revenue for this size class. Currency is Revenue Currency. null if this is not relevant to this size class. `Filter(eq)` 
| [Id](Crm.Marketing.CompanySizeClasses.md#id) | guid |  
| [Name](Crm.Marketing.CompanySizeClasses.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Company size class name (multi-language). `Required` `Filter(eq;like)` 
| [Notes](Crm.Marketing.CompanySizeClasses.md#notes) | string (max) __nullable__ | Notes for this CompanySizeClass. 
| [ObjectVersion](Crm.Marketing.CompanySizeClasses.md#objectversion) | int32 |  
| [ToEmployees](Crm.Marketing.CompanySizeClasses.md#toemployees) | int32 __nullable__ | Maximum number of employees for this size class. null if this is not relevant to this size class. `Filter(eq)` 
| [ToRevenue](Crm.Marketing.CompanySizeClasses.md#torevenue) | decimal (15, 0) __nullable__ | Maximal revenue for this size class. Currency is Revenue Currency. null if this is not relevant to this size class. `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [RevenueCurrency](Crm.Marketing.CompanySizeClasses.md#revenuecurrency) | [Currencies](General.Currencies.md) (nullable) | The currency in which the revenues are states. null if no revenues are specified. `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the CompanySizeClass. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### FromEmployees

Minimal number of employees for this size class. null if this is not relevant to this size class. `Filter(eq)`

_Type_: **int32 __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### FromRevenue

Minimal revenue for this size class. Currency is Revenue Currency. null if this is not relevant to this size class. `Filter(eq)`

_Type_: **decimal (15, 0) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Company size class name (multi-language). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this CompanySizeClass.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ToEmployees

Maximum number of employees for this size class. null if this is not relevant to this size class. `Filter(eq)`

_Type_: **int32 __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ToRevenue

Maximal revenue for this size class. Currency is Revenue Currency. null if this is not relevant to this size class. `Filter(eq)`

_Type_: **decimal (15, 0) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### RevenueCurrency

The currency in which the revenues are states. null if no revenues are specified. `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.CompanySizeClasses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.CompanySizeClasses erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_CompanySizeClasses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_CompanySizeClasses?$top=10>

