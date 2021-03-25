---
uid: Crm.Marketing.DistributionChannels
---
# Crm.Marketing.DistributionChannels Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

General list of distribution channels. Used to control prices and availability of products for the different channels. Entity: Crm_Distribution_Channels

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.Marketing.DistributionChannels.md#code) | string (10) | Unique distribution channel code. `Required` `Filter(eq;like)` 
| [Description](Crm.Marketing.DistributionChannels.md#description) | string (max) __nullable__ | Full description of the distribution channel. 
| [Id](Crm.Marketing.DistributionChannels.md#id) | guid |  
| [IsActive](Crm.Marketing.DistributionChannels.md#isactive) | boolean | Is the channel active for new sales? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)` 
| [Name](Crm.Marketing.DistributionChannels.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the distribution channel. `Required` `Filter(eq;like)` 


## Attribute Details

### Code

Unique distribution channel code. `Required` `Filter(eq;like)`

_Type_: **string (10)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **10**  

### Description

Full description of the distribution channel.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Is the channel active for new sales? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

Multi-language name of the distribution channel. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Marketing.DistributionChannels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.DistributionChannels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_DistributionChannels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_DistributionChannels?$top=10>

