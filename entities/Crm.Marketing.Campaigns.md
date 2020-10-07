# Crm.Marketing.Campaigns

Marketing campaigns. Used to treat target groups with marketing messages, plan budgets and marketing activities. Entity: Crm_Campaigns

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.Campaigns.md#Id) | guid |  
| [Name](Crm.Marketing.Campaigns.md#Name) | string | Short name of the campaign. [Required] [Filter(like)] [ORD] 
| [Description](Crm.Marketing.Campaigns.md#Description) | string (nullable) | Campaign description. 
| [EndDate](Crm.Marketing.Campaigns.md#EndDate) | datetime (nullable) | End date of the campaign. null means that the end date is still unknown. 
| [ForecastedCost](Crm.Marketing.Campaigns.md#ForecastedCost) | decimal | Forecasted total cost of the campaign. [Required] [Default(0)] 
| [StartDate](Crm.Marketing.Campaigns.md#StartDate) | datetime | Starting date of the campaign. [Required] [Default(Today)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> Short name of the campaign. [Required] [Filter(like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### Description

> Campaign description.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EndDate

> End date of the campaign. null means that the end date is still unknown.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ForecastedCost

> Forecasted total cost of the campaign. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StartDate

> Starting date of the campaign. [Required] [Default(Today)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  



## Business Rules

[!list erp.entity=Crm.Marketing.Campaigns erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Marketing.Campaigns erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Marketing.Campaigns erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_Campaigns?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_Campaigns?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Campaigns?$top=10>

