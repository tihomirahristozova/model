---
uid: Finance.Cost.CostTypes
---
# Finance.Cost.CostTypes Entity

Types of costs. Entity: Cost_Types

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Cost.CostTypes.md#code) | string | Unique cost type code. Used for charting. [Required] [Filter(eq)] [ORD] 
| [Id](Finance.Cost.CostTypes.md#id) | guid |  
| [Name](Finance.Cost.CostTypes.md#name) | string | Multilanguage cost type name. [Required] [Filter(like)] 


## Attribute Details

### Code

Unique cost type code. Used for charting. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage cost type name. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Cost.CostTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.CostTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CostTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CostTypes?$top=10>

