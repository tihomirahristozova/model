---
uid: Crm.Marketing.DistributionChannels
---
# Crm.Marketing.DistributionChannels

General list of distribution channels. Used to control prices and availability of products for the different channels. Entity: Crm_Distribution_Channels

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.DistributionChannels.md#Id) | guid |  
| [Description](Crm.Marketing.DistributionChannels.md#Description) | string (nullable) | Full description of the distribution channel. 
| [Code](Crm.Marketing.DistributionChannels.md#Code) | string | Unique distribution channel code. [Required] [Filter(eq;like)] 
| [Name](Crm.Marketing.DistributionChannels.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multi-language name of the distribution channel. [Required] [Filter(eq;like)] 
| [IsActive](Crm.Marketing.DistributionChannels.md#IsActive) | boolean | Is the channel active for new sales? true=Yes, false=No. [Required] [Default(true)] [Filter(eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> Full description of the distribution channel.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Unique distribution channel code. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Multi-language name of the distribution channel. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### IsActive

> Is the channel active for new sales? true=Yes, false=No. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  



## Business Rules

[!list erp.entity=Crm.Marketing.DistributionChannels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.DistributionChannels erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Marketing.DistributionChannels erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_DistributionChannels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_DistributionChannels?$top=10>

